---
title: Quotes
description: Streamer.bot has a built in quote system. It allows to add, display and delete quotes. Adding a quote automatically assigns an ID and saves a timestamp, the quoting user, the platform as well as the current category (like "Just Chatting").
---

## Setup
In order to use the built in quote system, navigate to `Settings -> Quotes` and check `Enabled`. 

![Quote Settings](assets/quotes_6.png)

In here you'll see all quotes that have been added to your Streamer.bot already and you'll also be able to change the permissions to add quotes. 

![Quote Permissions](assets/quotes_2.png)

::tip
Deleting quotes is reserved for the broadcaster and moderators only.
::

And you're all done already!

## Commands
The quote commands are also already built in. So you don't need to create any extra commands.

`!quote add [Quote]`

Adds the quote.

`!quote del [Quote ID]`

Deletes the specified quote.

`!quote [Quote ID]`

Shows the specified quote in chat.

`!quote`

Shows a random quote in chat.

::tip
You'll need a `Show Quote` trigger to display quotes in chat. See below.
::

### Triggers
You can add triggers for adding and showing quotes.

1. Quote Added
   
   The "Quote Added" trigger fires whenever you add a quote. It's totally optional, but you can use it to give a chat response that quote X has been successfully added.

   ![Quote Added](assets/quotes_3.png)

3. Show Quote
   
   The "Show Quote" fires upon entering the `!quote` or `!quote [Quote ID]` command. To display quotes in chat, that one is required. This trigger already handles specific and random quotes automatically.

   ![Quote Added](assets/quotes_4.png)


![Quote Added](assets/quotes_5.png)

## Usage
:api-reference-cards{path=core/quotes}
