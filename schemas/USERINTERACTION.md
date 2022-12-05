# User Interaction Schema

```
additionalType will be:
  - https://zion.fyi/Like
  - https://zion.fyi/Favorite
  - https://zion.fyi/Boost
```

```ts
interface UserInteraction {
  actor Person
  identifier string //uuid v4 identifier of this content
  additionalType string // schema key(url) of interaction type
  text string // the interaction content json encoded
  dateCreated DateTime // date time object for created
}
```