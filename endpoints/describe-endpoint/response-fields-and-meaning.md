---
description: Response fields and their meaning for the describe endpoint.
---

# Describe Endpoint - Response Fields & Meaning

<table>
    <thead>
        <tr>
            <th>Field Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>element</td>
            <td>Indicates that the object represents a station.</td>
        </tr>
        <tr>
            <td>guide_id</td>
            <td>The unique ID of the station used by Radiotime.</td>
        </tr>
        <tr>
            <td>preset_id</td>
            <td>The unique ID of the station used by TuneIn.</td>
        </tr>
        <tr>
            <td>name</td>
            <td>The name of the station.</td>
        </tr>
        <tr>
            <td>call_sign</td>
            <td>The call sign of the station.</td>
        </tr>
        <tr>
            <td>slogan</td>
            <td>The slogan or tagline of the station.</td>
        </tr>
        <tr>
            <td>frequency</td>
            <td>The frequency of the station's broadcast.</td>
        </tr>
        <tr>
            <td>band</td>
            <td>The band (e.g. FM, AM) on which the station broadcasts.</td>
        </tr>
        <tr>
            <td>url</td>
            <td>The website URL of the station.</td>
        </tr>
        <tr>
            <td>report_url</td>
            <td>The URL of the TuneIn contact form for reporting issues with the station.</td>
        </tr>
        <tr>
            <td>detail_url</td>
            <td>The URL of the TuneIn station detail page.</td>
        </tr>
        <tr>
            <td>is_preset</td>
            <td>Indicates whether the station is a TuneIn preset station.</td>
        </tr>
        <tr>
            <td>is_available</td>
            <td>Indicates whether the station is currently available.</td>
        </tr>
        <tr>
            <td>is_music</td>
            <td>Indicates whether the station plays music.</td>
        </tr>
        <tr>
            <td>has_song</td>
            <td>Indicates whether the station is currently playing a song.</td>
        </tr>
        <tr>
            <td>has_schedule</td>
            <td>Indicates whether the station has a schedule of programming.</td>
        </tr>
        <tr>
            <td>has_topics</td>
            <td>Indicates whether the station has topic-based programming.</td>
        </tr>
        <tr>
            <td>twitter_id</td>
            <td>The Twitter handle of the station.</td>
        </tr>
        <tr>
            <td>logo</td>
            <td>The URL of the station's logo.</td>
        </tr>
        <tr>
            <td>location</td>
            <td>The location of the station.</td>
        </tr>
        <tr>
            <td>current_song</td>
            <td>The currently playing song on the station, if available.</td>
        </tr>
        <tr>
            <td>current_artist</td>
            <td>The artist of the currently playing song on the station, if available.</td>
        </tr>
        <tr>
            <td>current_artist_id</td>
            <td>The unique ID of the artist of the currently playing song on the station, if available.</td>
        </tr>
        <tr>
            <td>current_album</td>
            <td>The album of the currently playing song on the station, if available.</td>
        </tr>
        <tr>
            <td>current_artist_art</td>
            <td>The URL of the artist image for the currently playing song on the station, if available.</td>
        </tr>
        <tr>
            <td>current_album_art</td>
            <td>The URL of the album cover image for the currently playing song on the station, if available.</td>
        </tr>
        <tr>
            <td>description</td>
            <td>A description of the station.</td>
        </tr>
        <tr>
            <td>email</td>
            <td>The email address of the station.</td>
        </tr>
        <tr>
            <td>phone</td>
            <td>The phone number of the station.</td>
        </tr>
        <tr>
            <td>mailing_address</td>
            <td>The mailing address of the station.</td>
        </tr>
        <tr>
            <td>language</td>
            <td>The language(s) spoken on the station.</td>
        </tr>
        <tr>
            <td>genre_id</td>
            <td>The unique ID of the station's genre.</td>
        </tr>
        <tr>
            <td>genre_name</td>
            <td>The name of the station's genre.</td>
        </tr>
        <tr>
            <td>region_id</td>
            <td>The unique ID of the station's region.</td>
        </tr>
        <tr>
            <td>country_region_id</td>
            <td>The unique ID of the station's country region.</td>
        </tr>
        <tr>
            <td>latlon</td>
            <td>The latitude and longitude of the station</td>
        </tr>
        <tr>
            <td>region_id</td>
            <td>The unique ID of the region.</td>
        </tr>
        <tr>
            <td>country_region_id</td>
            <td>The ID of the country/region.</td>
        </tr>
        <tr>
            <td>latlon</td>
            <td>The latitude and longitude of the station.</td>
        </tr>
        <tr>
            <td>tz</td>
            <td>The time zone of the station.</td>
        </tr>
        <tr>
            <td>tz_offset</td>
            <td>The time zone offset in minutes.</td>
        </tr>
        <tr>
            <td>publish_song</td>
            <td>Whether the station is currently publishing a song.</td>
        </tr>
        <tr>
            <td>publish_song_url</td>
            <td>The URL of the currently published song.</td>
        </tr>
        <tr>
            <td>publish_song_rejection_reason</td>
            <td>The reason why the song publishing was rejected.</td>
        </tr>
        <tr>
            <td>now_playing_url</td>
            <td>The URL of the now playing data.</td>
        </tr>
        <tr>
            <td>external_key</td>
            <td>The external key of the station.</td>
        </tr>
        <tr>
            <td>ad_eligible</td>
            <td>Whether the station is eligible for ads.</td>
        </tr>
        <tr>
            <td>preroll_ad_eligible</td>
            <td>Whether the station is eligible for preroll ads.</td>
        </tr>
        <tr>
            <td>companion_ad_eligible</td>
            <td>Whether the station is eligible for companion ads.</td>
        </tr>
        <tr>
            <td>video_preroll_ad_eligible</td>
            <td>Whether the station is eligible for video preroll ads.</td>
        </tr>
        <tr>
            <td>fb_share</td>
            <td>Whether the station can be shared on Facebook.</td>
        </tr>
        <tr>
            <td>twitter_share</td>
            <td>Whether the station can be shared on Twitter.</td>
        </tr>
        <tr>
            <td>song_share</td>
            <td>Whether the currently playing song can be shared.</td>
        </tr>
        <tr>
            <td>donation_eligible</td>
            <td>Whether the station is eligible for donations.</td>
        </tr>
        <tr>
            <td>donation_url</td>
            <td>The URL to donate to the station.</td>
        </tr>
        <tr>
            <td>donation_text</td>
            <td>The text displayed to ask for donations.</td>
        </tr>
        <tr>
            <td>donation_icon</td>
            <td>The URL of the donation icon.</td>
        </tr>
        <tr>
            <td>song_buy_eligible</td>
            <td>Whether the currently playing song is eligible for purchase.</td>
        </tr>
        <tr>
            <td>tunein_url</td>
            <td>The URL of the station on TuneIn.</td>
        </tr>
        <tr>
            <td>is_family_content</td>
            <td>Whether the station's content is family-friendly.</td>
        </tr>
        <tr>
            <td>is_mature_content</td>
            <td>Whether the station's content is mature.</td>
        </tr>
        <tr>
            <td>is_event</td>
            <td>Whether the station is an event.</td>
        </tr>
        <tr>
            <td>content_classification</td>
            <td>The classification of the station's content.</td>
        </tr>
        <tr>
            <td>echoed_count</td>
            <td>The number of echoes the station has received.</td>
        </tr>
        <tr>
            <td>favorited_count</td>
            <td>The number of times the station has been favorited.</td>
        </tr>
        <tr>
            <td>is_favorited</td>
            <td>Whether the station is favorited.</td>
        </tr>
        <tr>
            <td>is_favoritable</td>
            <td>Whether the station is favoritable.</td>
        </tr>
        <tr>
            <td>has_profile</td>
            <td>Whether the station has a profile.</td>
        </tr>
        <tr>
            <td>can_cast</td>
            <td>Whether the station can be casted.</td>
        </tr>
        <tr>
            <td>nielsen_eligible</td>
            <td>Whether the station is eligible for Nielsen ratings.</td>
        </tr>
        <tr>
            <td>nielsen_provider</td>
            <td>The provider of Nielsen ratings for the station.</td>
        </tr>
        <tr>
            <td>nielsen_asset_id</td>
            <td>The ID of the Nielsen asset for the station.</td>
        </tr>
        <tr>
            <td>nowplaying_channel</td>
            <td>The channel of the now playing data.</td>
        </tr>
        <tr>
            <td>why_ads_text</td>
            <td>The text explaining why ads are played on the station.</td>
        </tr>
        <tr>
            <td>use_native_player</td>
            <td>Whether the station uses a native player.</td>
        </tr>
        <tr>
            <td>live_seek_stream</td>
            <td>Whether the station supports live seeking.</td>
        </tr>
        <tr>
            <td>seek_disabled</td>
            <td>Whether seeking is disabled for the station.</td>
        </tr>
    </tbody>
</table>
