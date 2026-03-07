# 201_Read_11

- [HTML A/V](#html-av)
  - [`<video>` Element](#video-element)
    - [Sources](#sources)
    - [Features](#features)
    - [Video Text Tracks](#video-text-tracks)
  - [Answers.1](#answers1)
- [Grid Guide](#grid-guide)
- [Unresponsice HTML Images](#unresponsive-html-images)

## [HTML A/V](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/HTML_video_and_audio)

Adding videos and audio was originally made possible through plugins (Flash and Silverlight), but now easily accessible through built-in HTML elements (`<video>` and `<audio>`) and javaScript APIs.

### `<video>` Element

```html
<video src="rabbit320.webm" controls>
  <p>
    Your browser doesn't support HTML video. Here is a
    <a href="rabbit320.webm">link to the video</a> instead.
  </p>
</video>
```

You should nest a `<p>` element inside the `<video>` element in order to provide fallback content, which works like `alt` text for an image, with the difference that it provides the source as a link rather than embedding it.

`controls` attribute is as it says, provides controls (pause, play, forward, backward, etc.) for playback. Can be supplemented with JS APIs.

#### Sources

Not all browsers play and support the same video formats. Each browser also supports a range of varying codecs that convert to and from compressed a/v and binary. To ensure media will be compatible and play on browser, prepare to provide multiple formats and do [research](https://developer.mozilla.org/en-US/docs/Web/Media/Guides/Formats/Containers#choosing_the_right_container) on [video](https://developer.mozilla.org/en-US/docs/Web/Media/Guides/Formats/Video_codecs#choosing_a_video_codec) and [audio](https://developer.mozilla.org/en-US/docs/Web/Media/Guides/Formats/Audio_codecs#choosing_an_audio_codec) codecs.  

```html
<video controls>
  <source src="rabbit320.mp4" type="video/mp4" />
  <source src="rabbit320.webm" type="video/webm" />
  <p>
    Your browser doesn't support this video. Here is a
    <a href="rabbit320.mp4">link to the video</a> instead.
  </p>
</video>
```

Is what an updated `<video>` element would look like to account for different sources. It will go down the `<source>` elements for the first one that plays, the `type` attribute is optional, but encouraged to include and specify media type so browser may know which to prefer / skip those they don't understand.

#### Features

```html
controls
width="400"
height="400"
autoplay
loop
muted
preload="auto"
poster="poster.png">
```

are just a few of the other features one can specify when displaying a `<video>` element.  

`autoplay` is not recommended.  
`loop` will repeat media once finished.  
`muted` mutes by default.  
`poster` displays image of before video is played.
`preload` for large files. `'none'`, `'auto'`, and `'metadata'`.

#### Video Text Tracks

For when simply hearing the audio is not possible, for whichever reason, internal or external. Transcription is capable through [WebVTT](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API) format and `<track>` element.  

WebVTT format writes text files linked to the metadata of a video such as time in video, to keep the text synched.

### `<audio>` element

Works in same manner as `<video>` element.  
Differs in space taken up, less than a video since there is no visual; does not need / support `width` / `height`.  

### Answers.1

1. Explain how the ability to use video and audio on the web has evolved since the early 2000s.
    - Used to be done through plugins which had secuiryt concerns; nowadays its done through integarted html elements.
2. Describe the use of the `src` and `controls` attributes in the `<video>` element.
    - `src` points to the url or location of the video, whereas `controls` includes the controls for playback.
3. Why is it important to have fallback content inside the `<video>` element?
    - Not all browsers support the same formats and codecs.
4. Write a very short story where `<audio>` and `<video>` are characters.
    - two friends perform shows in houses across the city. The city is called the web and the house is the browser.  
    One friend performs his tale in a narrator fashion; sits in a chair, turns off the lights, provides blindfolds for the guests, and reads his story. The second friend has a stage, lights, props, outfits, and puts on a show for all to see.  
    The stories they perform at the each house vary and could be in any of the various languages and/or genres, it is up to the both of them to decide which show to put on for the guests and for the guests to decide on which night/house to attend the show.

## Grid Guide

## Unresponsive HTML Images
