---
description: Further information about the describe endpoint.
---

# 📃️ Describe Endpoint

## GET `/describe.ashx`

This is the endpoint that allows you to look up station information.

| Parameter | Example | Description              |
| --------- | ------- | ------------------------ |
| id        | s42069  | This is your station id. |

### Response

```xml
<opml version="1">
    <head>
        <status>200</status>

    </head>
    <body>
        <outline type="object" text="OctoStation">
            <station>
                <guide_id>s42069</guide_id>
                <preset_id>s42069</preset_id>
                <name>OctoStation</name>
                <call_sign>OctoStation</call_sign>
                <slogan>2 cool 4 a slogan!</slogan>
                <frequency>96.2</frequency>
                <band>FM</band>
                <url>http://www.octostation.com/</url>
                <report_url>http://tunein.com/contact/resolve/?stationId=42069</report_url>
                <detail_url>http://tun.in/abcDef</detail_url>
                <is_preset>false</is_preset>
                <is_available>true</is_available>
                <is_music>true</is_music>
                <has_song>false</has_song>
                <has_schedule>false</has_schedule>
                <has_topics>false</has_topics>
                <twitter_id>radioeksen</twitter_id>
                <logo>https://cdn-profiles.tunein.com/s42069/images/logoq.jpg?t=636445279591030000</logo>
                <location>Istanbul, Turkey</location>
                <description>Octo bass for your ears</description>
                <email>info@octostation.com</email>
                <phone>(420) 690 00 00</phone>
                <mailing_address>Someplace, TX, 53882 Texas Road</mailing_address>
                <language>English</language>
                <genre_id>g115</genre_id>
                <genre_name>Alternative Rock</genre_name>
                <region_id>r101125</region_id>
                <country_region_id>420690</country_region_id>
                <tz>GMT - 6 (Austin, Texas)</tz>
                <tz_offset>180</tz_offset>
                <ad_eligible>true</ad_eligible>
                <preroll_ad_eligible>true</preroll_ad_eligible>
                <companion_ad_eligible>false</companion_ad_eligible>
                <video_preroll_ad_eligible>false</video_preroll_ad_eligible>
                <fb_share>true</fb_share>
                <twitter_share>true</twitter_share>
                <song_share>true</song_share>
                <tunein_url>http://tunein.com/station/?stationId=42069</tunein_url>
                <is_family_content>false</is_family_content>
                <is_mature_content>false</is_mature_content>
                <is_event>false</is_event>
                <content_classification>music</content_classification>
                <has_profile>true</has_profile>
                <can_cast>true</can_cast>
                <nielsen_eligible>false</nielsen_eligible>
                <use_native_player>false</use_native_player>
                <live_seek_stream>false</live_seek_stream>
                <seek_disabled>false</seek_disabled>
            </station>
        </outline>
    </body>
</opml>
```

### Get station information

{% content-ref url="response-fields-and-meaning.md" %}
[response-fields-and-meaning.md](response-fields-and-meaning.md)
{% endcontent-ref %}
