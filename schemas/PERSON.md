# Person Schema
[Person Schema](https://schema.org/Person)
```ts
interface Person {
  identifier: string // DID identifier
  givenName: string // the person's first name
  familyName: string // the person's last name
  additionalName: string // display name
  image: Image // the user profile image object
  additionalType: string //reference to the additional zion user type.
}
```

```
https://zion.fyi/schemas/User
```

```ts
interface ZionUser {
  bio: string
  email: string
  status: string
}
```

[Person Schema DWN Messages](../d-web-nodes/person/)
