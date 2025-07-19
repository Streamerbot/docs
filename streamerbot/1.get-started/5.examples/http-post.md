---
title: Advanced "Fetch URL"
description: Send web requests manually using HTTPClient.
author: ErinaSugino
icon: i-mdi-web-plus
navigation: false
difficulty: 2
---

StreamerBot already has the built-in [Fetch URL](/api/sub-actions/core/network/fetch-url) sub-action to immediately send simple HTTP `GET` requests directly from the actions UI.

Sometimes, however, you will find a situation where you need to send data via `POST`, `PUT` or generally any other request type that is *not* `GET`.

In this case, you will need to implement your own request handling in a C# code module using the [HttpClient](https://learn.microsoft.com/en-us/dotnet/api/system.net.http.httpclient?view=net-9.0){target=_blank rel=noopener} class.

::read-more{to="/api/core/csharp/execute-csharp-code"}
Read more about the `Execute C# Code` sub-action
::

## Prerequisites

1. Basic understanding of writing C# code

    Since all of this *has* to be implemented in a C# code module, basic understanding of writing C# code and using common libraries is required. I will only give the most basic example, you will likely need to adapt it to your usecase.

2. Understanding on how to use C# in sub-actions

    Be it a single use `Execute C# Code` block for a single instance of needing to send a request, or a more persistent C# module with different actions triggering different `Execute C# Method` sub-actions - you need to know how use this feature in your normal action flow.

    The following tutorial will only focus on the magic happening inside of the C# code module.

## Instructions

1. Setup the HTTPClient

  ```cs [Basic Setup]
  using System;
  using System.Text;
  using System.Threading.Tasks;
  using System.Net.Http;
  using System.Net.Http.Headers;
  using Newtonsoft.Json;
  using Newtonsoft.Json.Linq;

  public class CPHInline {
    // You can set the timeout to any length you need
    private static readonly HttpClient _httpClient = new HttpClient{Timeout = TimeSpan.FromSeconds(30)};

    public void Init() {
      // Ensure we are working with a clean slate
      _httpClient.DefaultRequestHeaders.Clear();
    }

    public void Dispose() {
      // Free up allocations
      _httpClient.Dispose();
    }

    public bool Execute() {
      // ...
      return true;
    }
  }
  ```

  ::tip{color=amber}
  While people using the HTTPClient in a `using` statement or creating a new one within the executed function may be a common occurence, it is heavily discouraged to do so. [Read More](https://extensions.streamer.bot/t/httpclient-and-you/1369)
  ::

2. Setup the sending of your payload

  We are going to send a `%userName%` and `%userId%` pair (from common triggers) as `PUT` request to our fictional logging website.

  ```cs [Send PUT payload in Execute method]
  public bool Execute() {
    // Get the arguments - or abort if it does not exist
    if(!CPH.TryGetArg("userName", out string userName)) return false;
    if(!CPH.TryGetArg("userId", out string userId)) return false;

    // Build a wrapper object as payload
    var data = new {
      id = userId,
      name = userName
    };

    // Serialize JSON
    string json = JsonConvert.SerializeObject(data);

    // Create web request payload
    var payload = new StringContent(json, Encoding.UTF8, "application/json");

    // Finally, send request
    HttpResponseMessage response = _httpClient.PutAsync("https://my-logging-server.com", payload).GetAwaiter().GetResult();

    // Do with the response what you need to.
    // ...

    return true;
  }
  ```

  - To use different request types, simply use the methods `GetAsync()`, `PutAsync()`, `PostAsync()` or `DeleteAsync()`.

3. The PATCH request

  Specifically the built-in handling for the `PATCH` request type may not be available in the .net versions used by StreamerBot. In this case, you need a workaround.

  ```cs [PATCH workaround]
    // ...

    // Finally, send the request
    var request = new HttpRequestMessage(new HttpMethod("PATCH"), "https://my-logging-server.com"){
      Content = payload
    };
    HttpResponseMessage response = _httpClient.SendAsync(request).GetAwaiter().GetResult();

    // ...
  ```

4. Additional Headers

  If you need to additionally include specific headers - like submitting an authorization token for the Twitch API or Discord API - make sure to clear and set the headers on each call you make.
  
  You can also send individual headers with each request itself, but that requires you to always use the `SendAsync` method and building your own `HttpRequestMessage`.

  If your code only does a static request whose headers never change, resetting the headers is **not strictly necessary**. But it's good practice to not forget later when you need it.

  ```cs [Header management]
  public bool Execute() {
    // Making a call to the Twitch API to get all currently live streams
    string token = CPH.TwitchOAuthToken;
    string clientId = CPH.TwitchClientId;

    // Clear our old headers
    _httpClient.DefaultRequestHeaders.Clear();

    // Now set your Twitch API authorization
    _httpClient.DefaultRequestHeaders.Add("Authorization", "Bearer "+token);
    _httpClient.DefaultRequestHeaders.Add("Client-Id", clientId);

    // Send your request
    HttpResponseMessage response = _httpClient.GetAsync("https://api.twitch.tv/helix/streams").GetAwaiter().GetResult();

    // Do with the response what you need to.
    // ...

    return true;
  }
  ```

5. Handling the response

  Since you have to do the entire request handling yourself, that includes handling the response.
  
  If you don't need to know what the server responded, you can ignore it like in the examples above.
  
  If you need to know if the request succeeded or are expecting data in return, follow the below example.

  ```cs [Response handling]
  public bool Execute() {
    // ...all your data preparation

    HttpResponseMessage response = _httpClient.GetAsync("https://api.twitch.tv/helix/streams").GetAwaiter().GetResult();

    // Check if our request was successful
    try {
      if(!response.IsSuccessStatusCode) {
        // It was not. Abort.
        CPH.LogError($"{response.StatusCode} - {response.ReasonPhrase}");
        return false;
      }

      // Get the response data
      string content = response.Content.ReadAsStringAsync().GetAwaiter().GetResult();

      // Usually, data is JSON. So you would decode it now.
      JObject parsed = JObject.Parse(content);

      // And then do with the data whatever you need.
      // ...

      return true;
    } catch (Exception e) {
      // Something went wrong
      CPH.LogError(e.Message);
      return false;
    }
  }
  ```

## Tips & Tricks

Wrapping sensitive parts of code, especially when using web requests, into `try` `catch` blocks is good practice and prevents potential unexpected bigger issues you do not anticipate.

Of course, proper error handling is always better, but not always necessary.