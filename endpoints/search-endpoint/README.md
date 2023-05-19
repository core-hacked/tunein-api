---
description: Further information about the search endpoint.
---

# 🔍 Search Endpoint

## GET `/search.ashx`

This is the endpoint that allows you to search on TuneIn.

| Parameter | Example | Description                                                                                                                 |
| --------- | ------- | --------------------------------------------------------------------------------------------------------------------------- |
| query     | GitFM   | This is your search query. It needs to be properly [URL escaped/encoded](https://www.w3schools.com/tags/ref_urlencode.ASP). |

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

### Genre IDs and their meanings.

{% content-ref url="genre-ids-and-meaning.md" %}
[genre-ids-and-meaning.md](genre-ids-and-meaning.md)
{% endcontent-ref %}

### Outline attributes and their meanings.

{% content-ref url="outline-attributes-and-meaning.md" %}
[genre-ids-and-meaning.md](outline-attributes-and-meaning.md)
{% endcontent-ref %}
