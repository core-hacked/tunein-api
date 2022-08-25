---
description: >-
  The attributes returned within the XML response inside of the 'outline'
  elements.
---

# 📂 Outline Attributes & Meaning

| Attribute        | Description                                                                                                                                               |
| ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| type             | This is the type of the displayed element.                                                                                                                |
| text             | This is the "text" or title of the element. It is usually the name of the station.                                                                        |
| URL              | This is the tune/streaming URL or a link to the corresponding page, depending on the type.                                                                |
| bitrate          | This is the bitrate of the station/stream. It's present if the element corresponds to a direct streaming URL.                                             |
| reliability      | This is the reliability score of the station/stream. The higher the better. It is a scale going from 0 to 100.                                            |
| guide\_id        | This seems to be the identifier for the stream and-/or current track/station.                                                                             |
| subtext          | This is the "subtext" or description of the station. Some stations use this as a way of displaying the currently playing song.                            |
| genre\_id        | This is the ID of the genre. [View a list of genre IDs and their genre.](search-endpoint/)                                                                |
| formats          | This is the format of the 'outline' element, usually mp3.                                                                                                 |
| show\_id         | This is the show/station id.                                                                                                                              |
| item             | Although the name, it also defines the type of the 'outline' element. See below for more information.                                                     |
| image            | The image of the radio station or podcast/show.                                                                                                           |
| current\_track   | The currently playing track, usually the same as the subtext.                                                                                             |
| now\_playing\_id | Probably the id of the currently playing track or the station.                                                                                            |
| preset\_id       | Usually the same as the now playing ID or Tune ID.                                                                                                        |
| playing\_image   | Some stations also stream the image of the currently playing song but it won't always be present.                                                         |
| has\_profile     | If the outline element in the search is an artist, this tells you if they have a profile on TuneIn you can visit.                                         |
| stream\_type     | If present it's usually `download`. It also usually means that the current element represents a topic and is a fixed audio file instead of a live stream. |
| topic\_duration  | This is the duration of the topic.                                                                                                                        |

### The `type` attribute and its possible values.

The `type` attribute defines the current outline element's type.\
Currently, it has three known values.

| Value | Description                                                                                                                         |
| ----- | ----------------------------------------------------------------------------------------------------------------------------------- |
| audio | This means that the outline element represents a station or show with a valid m3u file or in the case of a topic, valid m3u files.  |
| link  | This represents a link to another page, an artist's or station's profile, etc.                                                      |
| text  | This means that the element contains only text and usually does not have a URL corresponding to something.                          |

### The `item` attribute and its possible values.

The `item` attribute defines the current outline element's type.\
Currently, it has three known values.

| Value   | Description                                                                                                                                                                                |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| station | This means that the outline element represents a currently ongoing live stream. <mark style="color:yellow;">(live audio)</mark>                                                            |
| topic   | This means that the outline element represents an already passed live stream, that has been recorded or a part of an existing podcast. <mark style="color:yellow;">(non-live audio)</mark> |
| show    | This represents a collection of topics/a further link to audio elements of, ex. a podcast. <mark style="color:yellow;">(collection of non-live audios)</mark>                              |
