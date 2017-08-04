---
alias: quaingai0z
path: /docs/reference/relay-api/custom-mutations
layout: REFERENCE
shorttitle: Custom Mutations
description: Custom mutations can be added to your GraphQL API using Schema Extensions.
simple_relay_twin: thiele0aop
tags:
  - relay-api
  - mutations
related:
  further:
  more:
---

# Custom Mutations in the Relay API

Custom mutations can be added to your GraphQL API using [Schema Extensions]().

You can define the **name, input arguments and payload of the mutation** and **resolve it with a Graphcool Function**.

## Example

> Return a random number in a specified range

Schema Extension SDL document:

```graphql
type RandomNumberPayload {
  number: Float!
}

extend type Mutation {
  randomNumber(min: Int!, max: Int!): RandomNumberPayload
}
```

Graphcool Function:

```js
module.exports = function randomNumber(event) {
  const min = event.data.min
  const max = event.data.max

  if (min > max) {
    return {
      error: "Invalid input"
    }
  }

  const number = Math.random() * (max - min) + min

  return {
    data: {
      number
    }
  }
}
```

Then the mutation can be called like this using the Relay API:

```graphql
mutation {
  isValidAge(input: {
    age: 12
  }) {
    isValid # false
    age # 12
  }
}
```

Note that the returned object contains a `data` key, which in turn contains the `number` field that was specified in the `RandomNumberPayload` in the SDL document. [Error handling]() works similarly to other Graphcool Functions, if an object containing the `error` key is returned.
