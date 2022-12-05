# Post Schema
Schema URL:
```
https://schema.org/SocialMediaPosting
```
From [Social Media Posting](https://schema.org/SocialMediaPosting)
```ts
interface Post {
  identifier: string //uuid v4 identifier of this content
  author: Person // embedded "light" person schema of the author
  name: string // the post title
  text: string // the post content
  creativeWorkStatus: string // status of post
  dateCreated: DateTime // date time object for created
  dateModified: DateTime // date time object for edited initial same as created

  //AdditionalType allows you to add custom fields to a SocialMediaPosting
  additionalType: "https://zion.fyi/schemas/CommunityPost"
  additionalType: "https://zion.fyi/schemas/UserPost"
  additionalType: "https://zion.fyi/schemas/{SOME OTHER ADDITIONAL POST DATA}"

  // populated dynamically, not stored
  commentCount: number // eventually consistent comment counter

  //either generalize like this, or make a part of the CommunityPost/UserPost schema object
  interactionStatistic: number // eventually consistent interactions counter
  interactions: UserInteraction[] // an array of interactions to this post 
}

```

```ts
interface ZionPost {
  boostsSatoshis: string
  attachments: Attachment[]
}
```

```ts
//Inherits from ZionPost
interface CommunityPost {
  communityId: string //ID of the community referenced in the post.
  //... any other schema data related only to a community post
}

```

```ts
//Inherits from ZionPost
interface UserPost {
  userId: string //DID of the user related to this post
  //... any other schema data related only to a user post
}

```

[Post Schema DWN Messages](../d-web-nodes/post/)