# Kaldiras

> **Created by Antono**

Kaldiras is a video player for ReactJS. Simple, accessible, and easy to customize.

## Features
- Accessible, full support for VTT captions
- Customizable, change the color theming easily
- Fullscreen, supports native fullscreen
- Shortcut, supports keyboard shortcuts
- Playsinline, supports the playsinline attribute
- Playback Speed, adjust playback speed
- Multiple captions, support for multiple caption tracks
- Preview thumbnails, support for displaying preview thumbnails

## How to install
```bash
npm install kaldiras
```
or
```bash
yarn add kaldiras
```

## How to use
For now, Kaldiras supported video types like mp4, webm, mov, and ogg. You must set the video type on the source property and the quality size of the video.

The other property like subtitles and previews is optional. Just the source property is required.

```typescript
import "kaldiras/kaldiras.css";
import { Video } from "kaldiras";

const App = () => {
  return(
    <Video
    sources={[
      {
        source: "https://.../480p.mp4",
        type: "video/mp4",
        resolution: "1080"
      }
    ]}
    subtitles={[
      {
        label: "English",
        lang: "en",
        source: "https://.../en.vtt",
        default: true
      }
    ]}
    previews={[
      {
        source: "https://.../5s.png",
        time: "0:05"
      }
    ]} />
  )
}
```

### sources
Here will be explained the structure that exists in the sources property:

| key | type | description |
|--|--|--|
| source | ```string```  | Fill with the video url here. |
| type | ```video/mp4```, ```video/webm```, ```video/ogg```, ```video/quicktime``` | Set the video format. |
| resolution | ```360```, ```480```, ```576```, ```720```, ```1080```, ```1440```, ```2160``` | Set the video resolution. |
| default | ```boolean``` | Set the video with what resolution to display by default.  |


### subtitles
Here will be explained the structure that exists in the subtitles property:

| key | type | description |
|--|--|--|
| label | ```string``` | Fill with the caption language |
| lang | ```string``` | Fill with the caption language id |
| source | ```string``` | Fill with the caption url here. |
| default | ```boolean``` | Set the default caption. |


### previews
This property is used to display a thumbnail preview when highlighting the progress bar. Here will be explained the structure that exists in the previews property:

| key | type | description |
|--|--|--|
| source | ```string``` | Fill with the image url here. |
| time | ```string``` | Fill the time when the thumbnail shows, with a format ``m:ss``. |

## License
MIT © [Yudha Pratama Wicaksana](https://twitter.com/lordaur)
