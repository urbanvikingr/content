---
alias: zixaephoh8
path: /docs/reference/relay-api/traverse-many-nodes
layout: REFERENCE
shorttitle: Traversing many nodes
description: Traverse nodes in your query response by using edges. Available edges in the GraphQL schema depend on types and relations in your backend.
simple_relay_twin: ohree5pu0y
tags:
  - relay-api
  - queries
  - edges
  - relations
related:
  further:
  more:
---

# Traversing Many Nodes in the Relay API

In the Relay API, traversing edges connecting the current node to the many side of a relation works the same as for a one side of a relation. Simply select the relation field.

> Query information on all post nodes of a certain author node:

```graphql
---
endpoint: https://api.graph.cool/relay/v1/cixne4sn40c7m0122h8fabni1
disabled: false
---
query {
  viewer {
    User(id: "cixnekqnu2ify0134ekw4pox8") {
      id
      name
      posts {
        edges {
          node {
            id
            published
          }
        }
      }
    }
  }
}

---
{
  "data": {
    "viewer": {
      "User": {
        "id": "cixnekqnu2ify0134ekw4pox8",
        "name": "John Doe",
        "posts": {
          "edges": [
            {
              "node": {
                "id": "cixnen24p33lo0143bexvr52n",
                "published": false
              }
            },
            {
              "node": {
                "id": "cixnenqen38mb0134o0jp1svy",
                "published": true
              }
            },
            {
              "node": {
                "id": "cixneo7zp3cda0134h7t4klep",
                "published": true
              }
            }
          ]
        }
      }
    }
  }
}
```

The `posts` field exposes a further selection of properties that are defined on the `Post` type.

> Note: [Query arguments](!alias-on1yeiw7ph) for an inner field returning multiple nodes work similar as elsewhere.
