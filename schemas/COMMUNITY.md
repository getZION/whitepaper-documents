# Community Schema

Derived From [CreativeWorks Schema](https://schema.org/CreativeWork)

Schema URL:
```
  https://zion.fyi/Community
```

```ts
interface Community {
  id: string // ID of the Community
  name: string // Name of Community
  description: string // text description of the community
  thumbnailUrl: string // URL of the thumbnail
  image: Image // cover image
  creator: Person // The owner of this community
  creativeWorkStatus: string // Status of community

  // Not stored with data
  //referenced
  postCount: number // number of posts for this community

  // populated separately
  posts: Post[]
  members: Person[]
}
```




[Community Schema DWN Messages](../d-web-nodes/community/)
