---
description: >-
  Note, most of these endpoints won't be open to the public, but if you own the
  ender.site domain, you can use them at free will.
---

# 👨‍💻 API

{% api-method method="get" host="https://api.ender.site" path="" %}
{% api-method-summary %}
Free Tea
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free tea.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "message":"Naw man, no tea for you.",
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=418 %}
{% api-method-response-example-description %}
Tea successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "message":"I'm a teapot",
    "message2":"So am I!",
    "message3":"Really?",
    "message4":"Yeah!",
    "message5":"Woah that's awesome.",
    "message6":"Here's a teapot: https://api.ender.site/teapot"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.ender.site" path="/c/:channelId" %}
{% api-method-summary %}
View a channel
{% endapi-method-summary %}

{% api-method-description %}
Display data on a discord channel.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="channelId" type="string" required=true %}
Provide a valid channel ID.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
   "type":"text",
   "deleted":false,
   "id":"0123456789010",
   "name":"general",
   "rawPosition":1,
   "parentID":"00000000000000",
   "topic":"Testing channel!",
   "nsfw":false,
   "lastMessageID":"000000000000000",
   "rateLimitPerUser":0,
   "lastPinTimestamp":1420070400,
   "guild":"525056817399726102",
   "createdTimestamp":315536400
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.ender.site" path="/selectGuild" %}
{% api-method-summary %}
Dashboard: Select a guild
{% endapi-method-summary %}

{% api-method-description %}
Endpoint for the select guild page.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Token returned from Discord's OAuth
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.ender.site" path="/dash/:id" %}
{% api-method-summary %}
Dashboard
{% endapi-method-summary %}

{% api-method-description %}
Authorization required. Main dashboard page.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Authorization header
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="ID" type="string" required=true %}
Tells the server which dashboard to load.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
:^) This should change based on your auth token and ID.
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.ender.site" path="/bot/:guildId" %}
{% api-method-summary %}
Bot
{% endapi-method-summary %}

{% api-method-description %}
Checks if the bot is in the guild
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="guildId" type="string" required=false %}
Which guild ID to check.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Bot is in guild
{% endapi-method-response-example-description %}

```javascript
{"bot":1}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
Either bot has no permission to see guild, or bot is not in server.
{% endapi-method-response-example-description %}

```javascript
{"bot":0}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

