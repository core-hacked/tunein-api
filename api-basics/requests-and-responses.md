---
description: How to make requests to the Streaming API.
---

# ↔ Requests & Responses

### Methods of making requests

Sadly, TuneIn has a [same-origin policy](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin\_policy), that forbids you to access the API via JavaScript.\
However, you are still able to make requests using [cURL](https://en.wikipedia.org/wiki/CURL), [Postman](https://www.postman.com/), or other such software. This means that you can use PHP and its command execution functions to have a fully web-based radio streaming experience (although server-sided).

All requests are made using `GET` to the endpoint url.

### Authentication & Security

Although they have used a same-origin policy, they did not implement any authentication which means you can get started right away.&#x20;

You need to specify the protocol that you want to use (<mark style="color:red;">HTTP</mark>/ <mark style="color:green;">HTTPS</mark>) since there is no automatic redirection to https even if you/the client can fully support an https connection.

```batch
http://opml.radiotime.com | not secure by default.
https://opml.radiotime.com | secure and encrypted.
```

An example request using curl could look like the following:

```bash
curl -s -X GET "https://opml.radiotime.com/endpoint.ashx"
```

### API Responses

The API always responds with an XML Document which usually looks like this if you made a valid request.

{% code title="Response (valid request)" %}
```xml
<opml version="1">
    <head>
        <title>Some Title</title>
        <status>200</status>
    </head>
    <body>
        <outline attributes="something"/>
    </body>
</opml>
```
{% endcode %}

{% code title="Response (invalid request)" %}
```xml
<opml version="1">
    <head>
        <title>Invalid method</title>
        <status>404</status>
        <fault>Invalid method</fault>
        <fault_code>api.methodNotFound</fault_code>
    </head>
    <body> </body>
</opml>
```
{% endcode %}
