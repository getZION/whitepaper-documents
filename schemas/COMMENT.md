# Comment Schema

Schema URL:
```
https://schema.org/Comment
```
Derived From [Comment Schema](https://schema.org/Comment)

```ts
interface Comment {
  identifier: string //uuid v4 identifier of this content
  author: Person
  text: string // the comment content
  subjectOf: Post // the post this comment belongs to
  dateCreated: DateTime // date time object for created
  dateModified: DateTime // date time object for edited initial same as created

  //AdditionalType allows you to add custom fields to a SocialMediaPosting
  additionalType: "https://zion.fyi/schemas/Comment"

  // Not directly stored with the comment
  // references
  interactionsCount // number of interactions
  // populated separately 
  interactions UserInteraction[] // an array of interactions to this comment
}
```

```
https://zion.fyi/schemas/Comment
```

```ts
//derived from ZionPost ... doesn't need it's own definition possibly
interface ZionComment {
  // Relation Information here instead of subjectOf Field? 
  // Or keep subject of Field and infer object type by additionalType Field

  boostsSatoshis: string
  attachments: Attachment[]
}
```

[Comment Schema DWN Messages](../d-web-nodes/comment/)