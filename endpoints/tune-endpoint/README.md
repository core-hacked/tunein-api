---
description: Further information about the tune endpoint.
---

# 🎵 Tune Endpoint

## GET /`tune.ashx`

Get the `.m3u` file needed for streaming.&#x20;

| Parameter | Example  | Description                                                                                |
| --------- | -------- | ------------------------------------------------------------------------------------------ |
| id        | s12345   | This is the ID of the tune. You will get these from an outline objects attributes.         |
| sid       | p1234567 | <mark style="color:yellow;">Purpose unknown, used in combination with topics/shows.</mark> |

### Response

This endpoint is a direct download for the tune file with the .m3u extension. \
Learn more about the extension and how to use it/play music from it.

{% content-ref url="../intro-to-streaming/the-.m3u-extension.md" %}
[the-.m3u-extension.md](../intro-to-streaming/the-.m3u-extension.md)
{% endcontent-ref %}
