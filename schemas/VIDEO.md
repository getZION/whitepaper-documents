# Image Schema

```ts
interface Video {
  identifier: string //uuid v4 identifier of this content
  caption: string // optional caption
  thumbnail: Image // optional image object for the Video
  thumbnailURL: Image // optional url for the image of the video
  url: string // standard video url
  embedUrl: string // base64 encoded image data
}
```
> \* **contentUrl** and **embedUrl cannot** be set simultaneously 

We will currently only be storing a url of the image.