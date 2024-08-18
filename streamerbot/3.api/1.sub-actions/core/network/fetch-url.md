---
title: Fetch URL
description: Fetch a remote URL and retrieve the response body
parameters:
  - name: URL
    type: Text
    required: true
    description: |
      Enter the URL to fetch

      ::warning
      Only `GET` requests are supported at this time.<br>
      If you need support for additional methods such as `POST`, utilize C# sub-actions
      ::
  - name: Variable Name
    type: Text
    required: true
    description: Enter the name of the variable to store the response in
  - name: Parse result as JSON
    type: Toggle
    default: 'false'
    description: |
      Optionally parse the result as JSON

      Multiple variables will be populated, with the `Variable Name` you provided as the root key

      For example, a request to `https://catfact.ninja/fact`, with variable name `jsonResult`, would populate the variables `jsonResult.fact` and `jsonResult.length`.
  - name: Headers
    type: Table
    description: Optionally add custom headers to modify the HTTP request
variables:
  - name: <variableName>
    type: string
    description: |
      If _Parse result as JSON_ is **disabled**:

      The full text of the response body
    value: |
      {
        "fact": "Both humans and cats have identical regions in the brain responsible for emotion.",
        "length": 81
      }
  - name: <variableName>.<jsonKey>
    description: |
      If _Parse result as JSON_ is **enabled**:

      All json properties will be dynamically mapped to variables by key
    value: |
      <variableName>.fact: "Both humans and cats have identical regions in the brain responsible for emotion."
---

::tip
This sub-action behaves much like the URL commands in Nightbot and many other bots.
::
