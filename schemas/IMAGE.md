# Image Schema

```ts
interface Image {
  identifier: string //uuid v4 identifier of this content
  caption: string // optional caption
  url: string // standard image url
  embedUrl: string // base64 encoded image data
}
```
> \* **url** and contentUrl** and **embedUrl cannot** be set simultaneously 

We will currently only be storing a url of the image.