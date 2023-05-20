---
description: Response fields and their meaning for the describe endpoint.
---

# 📃 Response Fields & Meaning

| Field Name                       | Description                                                                                   |
| -------------------------------- | --------------------------------------------------------------------------------------------- |
| element                          | Indicates that the object represents a station.                                               |
| guide\_id                        | The unique ID of the station used by Radiotime.                                               |
| preset\_id                       | The unique ID of the station used by TuneIn.                                                  |
| name                             | The name of the station.                                                                      |
| call\_sign                       | The call sign of the station.                                                                 |
| slogan                           | The slogan or tagline of the station.                                                         |
| frequency                        | The frequency of the station's broadcast.                                                     |
| band                             | The band (e.g. FM, AM) on which the station broadcasts.                                       |
| url                              | The website URL of the station.                                                               |
| report\_url                      | The URL of the TuneIn contact form for reporting issues with the station.                     |
| detail\_url                      | The URL of the TuneIn station detail page.                                                    |
| is\_preset                       | Indicates whether the station is a TuneIn preset station.                                     |
| is\_available                    | Indicates whether the station is currently available.                                         |
| is\_music                        | Indicates whether the station plays music.                                                    |
| has\_song                        | Indicates whether the station is currently playing a song.                                    |
| has\_schedule                    | Indicates whether the station has a schedule of programming.                                  |
| has\_topics                      | Indicates whether the station has topic-based programming.                                    |
| twitter\_id                      | The Twitter handle of the station.                                                            |
| logo                             | The URL of the station's logo.                                                                |
| location                         | The location of the station.                                                                  |
| current\_song                    | The currently playing song on the station, if available.                                      |
| current\_artist                  | The artist of the currently playing song on the station, if available.                        |
| current\_artist\_id              | The unique ID of the artist of the currently playing song on the station, if available.       |
| current\_album                   | The album of the currently playing song on the station, if available.                         |
| current\_artist\_art             | The URL of the artist image for the currently playing song on the station, if available.      |
| current\_album\_art              | The URL of the album cover image for the currently playing song on the station, if available. |
| description                      | A description of the station.                                                                 |
| email                            | The email address of the station.                                                             |
| phone                            | The phone number of the station.                                                              |
| mailing\_address                 | The mailing address of the station.                                                           |
| language                         | The language(s) spoken on the station.                                                        |
| genre\_id                        | The unique ID of the station's genre.                                                         |
| genre\_name                      | The name of the station's genre.                                                              |
| region\_id                       | The unique ID of the station's region.                                                        |
| country\_region\_id              | The unique ID of the station's country region.                                                |
| latlon                           | The latitude and longitude of the station                                                     |
| region\_id                       | The unique ID of the region.                                                                  |
| country\_region\_id              | The ID of the country/region.                                                                 |
| latlon                           | The latitude and longitude of the station.                                                    |
| tz                               | The time zone of the station.                                                                 |
| tz\_offset                       | The time zone offset in minutes.                                                              |
| publish\_song                    | Whether the station is currently publishing a song.                                           |
| publish\_song\_url               | The URL of the currently published song.                                                      |
| publish\_song\_rejection\_reason | The reason why the song publishing was rejected.                                              |
| now\_playing\_url                | The URL of the now playing data.                                                              |
| external\_key                    | The external key of the station.                                                              |
| ad\_eligible                     | Whether the station is eligible for ads.                                                      |
| preroll\_ad\_eligible            | Whether the station is eligible for preroll ads.                                              |
| companion\_ad\_eligible          | Whether the station is eligible for companion ads.                                            |
| video\_preroll\_ad\_eligible     | Whether the station is eligible for video preroll ads.                                        |
| fb\_share                        | Whether the station can be shared on Facebook.                                                |
| twitter\_share                   | Whether the station can be shared on Twitter.                                                 |
| song\_share                      | Whether the currently playing song can be shared.                                             |
| donation\_eligible               | Whether the station is eligible for donations.                                                |
| donation\_url                    | The URL to donate to the station.                                                             |
| donation\_text                   | The text displayed to ask for donations.                                                      |
| donation\_icon                   | The URL of the donation icon.                                                                 |
| song\_buy\_eligible              | Whether the currently playing song is eligible for purchase.                                  |
| tunein\_url                      | The URL of the station on TuneIn.                                                             |
| is\_family\_content              | Whether the station's content is family-friendly.                                             |
| is\_mature\_content              | Whether the station's content is mature.                                                      |
| is\_event                        | Whether the station is an event.                                                              |
| content\_classification          | The classification of the station's content.                                                  |
| echoed\_count                    | The number of echoes the station has received.                                                |
| favorited\_count                 | The number of times the station has been favorited.                                           |
| is\_favorited                    | Whether the station is favorited.                                                             |
| is\_favoritable                  | Whether the station is favoritable.                                                           |
| has\_profile                     | Whether the station has a profile.                                                            |
| can\_cast                        | Whether the station can be casted.                                                            |
| nielsen\_eligible                | Whether the station is eligible for Nielsen ratings.                                          |
| nielsen\_provider                | The provider of Nielsen ratings for the station.                                              |
| nielsen\_asset\_id               | The ID of the Nielsen asset for the station.                                                  |
| nowplaying\_channel              | The channel of the now playing data.                                                          |
| why\_ads\_text                   | The text explaining why ads are played on the station.                                        |
| use\_native\_player              | Whether the station uses a native player.                                                     |
| live\_seek\_stream               | Whether the station supports live seeking.                                                    |
| seek\_disabled                   | Whether seeking is disabled for the station.                                                  |
