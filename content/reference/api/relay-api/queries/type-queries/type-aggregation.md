---
alias: umaxaqu4ei
path: /docs/reference/relay-api/type-aggregation
layout: REFERENCE
shorttitle: Type Aggregation Queries
description: For every available type in your GraphQL schema, certain queries are automatically generated.
simple_relay_twin: choh5leigh
tags:
  - relay-api
  - queries
  - type
related:
  further:
  more:
---

# Type Aggregation Queries in the Relay API

For every type in your GraphQL schema, different aggregation queries are available.

## Fetch the number of all nodes

> Count the number of all `User` nodes:

```graphql
---
endpoint: https://api.graph.cool/relay/v1/cixne4sn40c7m0122h8fabni1
disabled: false
---
query {
  viewer {
    allUsers {
      count
    }
  }
}
---
{
  "data": {
    "viewer": {
      "allUsers": {
        "count": 3
      }
    }
  }
}
```

## Count the number of nodes matching a certain filter condition

> Count the number of all `User` nodes with `accessRole` `ADMIN`:

```graphql
---
endpoint: https://api.graph.cool/relay/v1/cixne4sn40c7m0122h8fabni1
disabled: false
---
query {
  viewer {
    allUsers(filter: {
      accessRole: ADMIN
    }) {
      count
    }
  }
}
---
{
  "data": {
    "viewer": {
      "allUsers": {
        "count": 1
      }
    }
  }
}
```

## More Aggregation Options

Currently, count is the only available aggregation. For specific use cases, you can use [functions](!alias-boo6uteemo) to precalculate certain aggregations and update them when data changes.

Please join the discussion on [GitHub](https://github.com/graphcool/feature-requests/issues/70) if you are interested in a specific aggregation.
