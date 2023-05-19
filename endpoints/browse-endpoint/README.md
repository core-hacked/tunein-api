---
description: Further information about the browse endpoint.
---

# 🌐 Browse Endpoint

## GET `/`

If you request the base URI, you will receive a list of options you can pick from. (The browse categories) You can achieve the same result by requesting `/browse.ashx` without any GET parameters.

You can select any of these categories to browse further, see [browsing categories](../endpoints/browse-endpoint/browsing-categories.md).

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

## GET `/browse.ashx`

Browse inside of a category. You can also view all categories by requesting the browse endpoint without any GET parameters.

| Parameter | Example | Description                                                                                             |
| --------- | ------- | ------------------------------------------------------------------------------------------------------- |
| c         | local   | This is the browse category.                                                                            |
| id        | r0      | This is the id of the country or continent. r0 corresponds to the continent selection.                  |
| filter    | l203    | Used by the language category to filter. <mark style="color:yellow;">(Meaning unknown as of now)</mark> |

{% hint style="info" %}
For all possible parameter values, see [Browsing Categories](../endpoints/browse-endpoint/browsing-categories.md), [Browse Location IDs](../endpoints/browse-endpoint/browse-location-ids.md), or [The Filter Parameter](../endpoints/browse-endpoint/filter-parameter.md).
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

### Browsing Categories

{% content-ref url="browsing-categories.md" %}
[browsing-categories.md](browsing-categories.md)
{% endcontent-ref %}

### Browse Location IDs

{% content-ref url="browse-location-ids.md" %}
[browse-location-ids.md](browse-location-ids.md)
{% endcontent-ref %}

### Information about the `filter` parameter

{% content-ref url="filter-parameter.md" %}
[filter-parameter.md](filter-parameter.md)
{% endcontent-ref %}
