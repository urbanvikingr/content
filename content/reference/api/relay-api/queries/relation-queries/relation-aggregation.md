---
alias: fe1ahseek6
path: /docs/reference/relay-api/relation-aggregation
layout: REFERENCE
shorttitle: Relation Aggregation
description: For every available relation in your GraphQL schema, certain queries are automatically generated.
simple_relay_twin: taesee4ua7
tags:
  - relay-api
  - queries
  - edges
  - relations
related:
  further:
  more:
---

# Relation Aggregation in the Relay API

Relay connections expose meta information for relations.

> Query meta information on all post nodes of a certain author node:

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
        count
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
          "count": 3
        }
      }
    }
  }
}
```

> Query meta information on certain post nodes of a certain author node:

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
      posts(filter: {
        title_contains: "adventure"
      }) {
        count
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
          "count": 1
        }
      }
    }
  }
}
```
