---
description: Learn how to extract a streaming url from an M3U File and play music from it.
---

# ❓ How to Stream

## Streaming in Linux.

Streaming inside of Linux is very simple, you can use `xdg-open` to find an app that supports this format by giving it the `Tune.m3u` file directly. You can view an implemented search and player made in bash on GitHub.&#x20;

### [Tunejack.sh](https://gist.github.com/xndc/c732204e274743204f1f)

&#x20;Instant radio streaming script using the TuneIn API by xndc.

## Streaming on non-Linux devices or the web.

To start off here, although some players support the M3U format, there is a simple way to do it on all platforms.

### URL Extraction and Usage.

If your player does not support M3U or you don't want to install additional software, you can extract the URL from the m3u file by simply viewing it inside of a text editor.&#x20;

It should give you a URL or multiple <mark style="color:yellow;">(some stations/streams have varying qualities)</mark> that you can open inside of your web browser to give you an mp3 audio control.&#x20;

You can also use this inside of an HTML <mark style="color:green;">`<audio>`</mark> tag, to play music on your own website.

```html
<audio controls autoplay>
    <source src="https://stream.url" type="audio/mpeg">
</audio>
```

{% hint style="info" %}
This is pretty much the basis for streaming, if you need the "rich" streaming experience, you will need to create a parser that can display this either in HTML or some other language you want.
{% endhint %}
