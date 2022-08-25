---
description: Information about the filter parameter.
---

# 🔎 Filter Parameter

{% hint style="warning" %}
The filter parameter and its capabilities are currently not fully discovered some parts are hidden within the API but it will be guesswork to find all possible filters.

If you happen to have information about the filters or have discovered a new one, please [kindly contribute](https://github.com/core-hacked/tunein-api/pulls) to the project's documentation.
{% endhint %}

This part of the documentation aims to find and document the various filter options of the API.&#x20;

> Most of the filter are weird but a pattern that is noticed between all of them is `letter:text`
>
> Two known examples of this are: `s:popular` and `p:show`

{% hint style="info" %}
These do not seem to work unless you search by an ID of something with a filter. Example: you filter by language and set the filter to be popular stations.
{% endhint %}

> The three main types for the `p:` filter are `show, station, topic.`
>
> These are the three return values found when looking at the `item` attribute of the outline elements within the response.

### Helpful resources and some basis for the documentation.

{% content-ref url="../../../credits-basis-and-helpful-resources/credits-basis-and-helpful-resources.md" %}
[credits-basis-and-helpful-resources.md](../../../credits-basis-and-helpful-resources/credits-basis-and-helpful-resources.md)
{% endcontent-ref %}
