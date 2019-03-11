# 🚧 API Work in Progress

{% api-method method="get" host="https://api.ender.site" path="/" %}
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



