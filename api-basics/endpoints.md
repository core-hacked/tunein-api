---
description: The different endpoints that TuneIn uses to communicate with the API.
---

# 🔗 Endpoints

{% hint style="warning" %}
Endpoint Information may be incomplete. If you have more information please [contribute.](https://github.com/core-hacked/tunein-api/pulls)
{% endhint %}

## Browse options

### GET `/`

If you request the base URI, you will receive a list of options you can pick from. (The browse categories) You can achieve the same result by requesting `/browse.ashx` without any GET parameters.

You can select any of these categories to browse further, see [browsing categories](../streaming-and-data/data-and-attributes/browse-endpoint/browsing-categories.md).

### Response

<pre class="language-xml"><code class="lang-xml">&#x3C;opml version="1">
<strong>    &#x3C;head>
</strong>        &#x3C;title>Browse&#x3C;/title>
        &#x3C;status>200&#x3C;/status>
    &#x3C;/head>
    &#x3C;body>
        &#x3C;outline type="link" text="Local Radio" URL="http://opml.radiotime.com/Browse.ashx?c=local" key="local"/>
        &#x3C;outline type="link" text="Music" URL="http://opml.radiotime.com/Browse.ashx?c=music" key="music"/>
        &#x3C;outline type="link" text="Talk" URL="http://opml.radiotime.com/Browse.ashx?c=talk" key="talk"/>
        &#x3C;outline type="link" text="Sports" URL="http://opml.radiotime.com/Browse.ashx?c=sports" key="sports"/>
        &#x3C;outline type="link" text="By Location" URL="http://opml.radiotime.com/Browse.ashx?id=r0" key="location"/>
        &#x3C;outline type="link" text="By Language" URL="http://opml.radiotime.com/Browse.ashx?c=lang" key="language"/>
        &#x3C;outline type="link" text="Podcasts" URL="http://opml.radiotime.com/Browse.ashx?c=podcast" key="podcast"/>
    &#x3C;/body>
&#x3C;/opml></code></pre>

## Search

### GET `/search.ashx`

This is the endpoint that allows you to search on TuneIn.

| Parameter | Example | Description                                                                                                                  |
| --------- | ------- | ---------------------------------------------------------------------------------------------------------------------------- |
| query     | GitFM   | This is your search query. It needs to be properly [URL escaped/encoded](https://www.w3schools.com/tags/ref\_urlencode.ASP). |

### Response

<pre class="language-xml" data-title="Results found."><code class="lang-xml">&#x3C;opml version="1">
    &#x3C;head>
        &#x3C;title>Search Results: GitFM&#x3C;/title>
        &#x3C;status>200&#x3C;/status>
<strong>    &#x3C;/head>
</strong>    &#x3C;body>
        &#x3C;outline type="link" text="Artist: GitFM" URL="http://opml.radiotime.com/Browse.ashx?id=a123456" guide_id="a123456" image="http://cdn-albums.tunein.com/gn/example.jpg" has_profile="false"/>
        &#x3C;outline type="audio" text="GitFM" URL="http://opml.radiotime.com/Tune.ashx?id=a12345" bitrate="128" reliability="99" guide_id="a12345" subtext="Octo - Git gud" genre_id="g61" formats="mp3" playing="Octo - Git gud" show_id="p1234567" item="station" image="http://cdn-profiles.tunein.com/a12345/images/logoq.jpg?t=123456" current_track="C-Section" now_playing_id="a12345" preset_id="a12345"/>
    &#x3C;/body>
&#x3C;/opml></code></pre>

{% code title="Results not found." overflow="wrap" %}
```xml
<opml version="1">
    <head>
        <title>Search Results: GitFM</title>
        <status>200</status>
    </head>
    <body>
        <outline type="text" text="No results for GitFM"/>
    </body>
</opml>
```
{% endcode %}

## Browsing

### GET `/browse.ashx`

Browse inside of a category. You can also view all categories by requesting the browse endpoint without any GET parameters.

| Parameter | Example | Description                                                                                             |
| --------- | ------- | ------------------------------------------------------------------------------------------------------- |
| c         | local   | This is the browse category.                                                                            |
| id        | r0      | This is the id of the country or continent. r0 corresponds to the continent selection.                  |
| filter    | l203    | Used by the language category to filter. <mark style="color:yellow;">(Meaning unknown as of now)</mark> |

{% hint style="info" %}
For all possible parameter values, see [Browsing Categories](../streaming-and-data/data-and-attributes/browse-endpoint/browsing-categories.md), [Browse Location IDs](../streaming-and-data/data-and-attributes/browse-endpoint/browse-location-ids.md), or [The Filter Parameter](../streaming-and-data/data-and-attributes/browse-endpoint/filter-parameter.md).
{% endhint %}

### Response

{% code title="Category: local" %}
```xml
<opml version="1">
    <head>
        <title>Local Radio</title>
        <status>200</status>
    </head>
    <body>
        <outline text="Stations" key="stations">
            <outline type="audio" text="OctoStation" URL="http://opml.radiotime.com/Tune.ashx?id=s100000" bitrate="128" reliability="99" guide_id="s100000" subtext="TuneOut - Music" genre_id="g61" formats="mp3" show_id="p1225767" item="station" image="http://cdn-profiles.tunein.com/s12345/images/logoq.jpg?t=155664" current_track="TuneOut - Music" now_playing_id="s100000" preset_id="s100000"/>
        </outline>
    </body>
</opml>
```
{% endcode %}

## Tune Request API

### GET /`tune.ashx`

Get the `.m3u` file needed for streaming.&#x20;

| Parameter | Example  | Description                                                                                |
| --------- | -------- | ------------------------------------------------------------------------------------------ |
| id        | s12345   | This is the ID of the tune. You will get these from an outline objects attributes.         |
| sid       | p1234567 | <mark style="color:yellow;">Purpose unknown, used in combination with topics/shows.</mark> |

### Response

This endpoint is a direct download for the tune file with the .m3u extension. \
Learn more about the extension and how to use it/play music from it.

{% content-ref url="../streaming-and-data/intro-to-streaming/the-.m3u-extension.md" %}
[the-.m3u-extension.md](../streaming-and-data/intro-to-streaming/the-.m3u-extension.md)
{% endcontent-ref %}
