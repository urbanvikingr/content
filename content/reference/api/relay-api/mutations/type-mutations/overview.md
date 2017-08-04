---
alias: iequie1oxi
path: /docs/reference/relay-api/type-mutations
layout: REFERENCE
shorttitle: Type Mutations
description: For every available type in your GraphQL schema, certain mutations are automatically generated.
simple_relay_twin: eamaiva5yu
tags:
  - simple-api
  - mutations
related:
  further:
  more:
---

# Type Mutations in the Relay API

For every available [type](!alias-ij2choozae) in your [GraphQL schema](!alias-ahwoh2fohj), certain mutations are automatically generated.

For example, if your schema contains a `Post` type:

```graphql
type Post {
  id: ID!
  title: String!
  description: String
}
```

the following type mutations will be available:

* the `createPost` mutation [creates a new node]().
* the `updatePost` mutation [updates an existing node]().
* the `deletePost` mutation [deletes an existing node]().
