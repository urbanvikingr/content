---
alias: oiviev0xi7
path: /docs/reference/relay-api/queries
layout: REFERENCE
description: Use queries to fetch data. Queries in the GraphQL schema of your project are derived from types and relations that you defined.
simple_relay_twin: nia9nushae
tags:
  - relay-api
  - queries
related:
  further:
    - vah0igucil
    - aizoong9ah
  more:
    - cahzai2eur
---

# Queries in the Relay API

A *GraphQL query* is used to fetch data from a GraphQL [endpoint](!alias-yahph3foch#project-endpoints). This is an example query:

```graphql
---
endpoint: https://api.graph.cool/relay/v1/cixne4sn40c7m0122h8fabni1
disabled: false
---
query {
  viewer {
    allPosts {
      edges {
        node {
          id
          title
          published
        }
      }
    }
  }
}
---
{
  "data": {
    "viewer": {
      "allPosts": {
        "edges": [
          {
            "node": {
              "id": "cixnen24p33lo0143bexvr52n",
              "title": "My biggest Adventure",
              "published": false
            }
          },
          {
            "node": {
              "id": "cixnenqen38mb0134o0jp1svy",
              "title": "My latest Hobbies",
              "published": true
            }
          },
          {
            "node": {
              "id": "cixneo7zp3cda0134h7t4klep",
              "title": "My great Vacation",
              "published": true
            }
          }
        ]
      }
    }
  }
}
```

Here's a list of available queries. To explore them, use the [playground](!alias-oe1ier4iej) inside your project.

* Based on the [types](!alias-ij2choozae) and [relations](!alias-goh5uthoc1) in your [GraphQL schema](!alias-ahwoh2fohj), [type queries](!alias-uquae2shae) and [relation queries](!alias-uo6uv0ecoh) will be generated to fetch type and relation data.
* Additionally, [custom queries](!alias-shae0xie0e) can be added to your API using [Schema Extensions](!alias-xohbu7uf2e).

Some queries support [query arguments](!alias-on1yeiw7ph) to further control the query response.
