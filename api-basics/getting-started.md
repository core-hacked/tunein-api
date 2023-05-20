---
description: Needed information on how to get started.
---

# 🤔 Getting Started

## Making requests and the limitations of the API

Sadly, TuneIn has a [same-origin policy](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin\_policy), that forbids you to access the API via JavaScript.\
However, you are still able to make requests using [cURL](https://en.wikipedia.org/wiki/CURL), [Postman](https://www.postman.com/), or other such software. This means that you can use PHP and its command execution functions to have a fully web-based radio streaming experience (although server-sided) or a custom software client/app.

All requests are made to the Base-URI defined in the [Introdcution](../) section, with the endpoints respective path appended and HTTP method specified before the path.

## Authentication & Security

Although TuneIn implemented a same-origin policy, they did not implement any authentication which means you can get started right away.

You need to specify the protocol that you want to use (<mark style="color:red;">HTTP</mark>/ <mark style="color:green;">HTTPS</mark>) since there is no automatic redirection to https even if you/the client can fully support an https connection.&#x20;

{% hint style="warning" %}
Keep in mind that all URLs given as a response by the API will start with <mark style="color:red;">`http://`</mark> no matter which protocol you requested. So you will need to replace <mark style="color:red;">`http://`</mark> with <mark style="color:green;">`https://`</mark> on your end to use <mark style="color:green;">HTTPS</mark>.
{% endhint %}

```batch
http://opml.radiotime.com | not secure by default.
https://opml.radiotime.com | secure and encrypted.
```

An example request using curl could look like the following:

```bash
# Docs: GET /endpoint.ashx
curl -s -X GET "https://opml.radiotime.com/endpoint.ashx"
```

## API Responses

The API always responds with an XML Document which usually looks something like this if you made a valid request.

{% code title="Response (valid request)" %}
```xml
<opml version="1">
    <head>
        <title>Some Title</title>
        <status>200</status>
    </head>
    <body>
        <outline type="audio" text="OctoStation" URL="http://opml.radiotime.com/Tune.ashx?id=a12345" bitrate="128" reliability="99" guide_id="s45087" subtext="OctoStation" genre_id="g61" formats="mp3" item="station" image="http://cdn-profiles.tunein.com/a12345/images/logoq.png" now_playing_id="a12345" preset_id="a12345"/>
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

## Alternative responses

Alternatively, you can add `&render=json` to the end of the request and render it in the json format. By default you will get an XML document. Other types of rendering have not yet been found. Feel free to add those into the documentation.

```bash
# Docs: GET /endpoint.ashx | with &render=json added
curl -s -X GET "https://opml.radiotime.com/endpoint.ashx&render=json"
```

{% code title="Response (valid request)" %}
```json
{
  "head": { "title": "Some title", "status": "200" },
  "body": [
    {
      "element": "outline",
      "type": "audio",
      "text": "OctoStation",
      "URL": "http://opml.radiotime.com/Tune.ashx?id=a12345",
      "bitrate": "128",
      "reliability": "99",
      "guide_id": "a12345",
      "subtext": "OctoStation",
      "genre_id": "g61",
      "formats": "mp3",
      "item": "station",
      "image": "http://cdn-profiles.tunein.com/a12345/images/logoq.png",
      "now_playing_id": "a12345",
      "preset_id": "a12345"
    }
  ]
}
```
{% endcode %}

{% code title="Response (invalid request)" %}
```json
{
  "head": {
    "title": "Invalid method",
    "status": "404",
    "fault": "Invalid method",
    "fault_code": "api.methodNotFound"
  },
  "body": []
}
```
{% endcode %}
