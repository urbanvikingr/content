---
alias: kaegh4oomu
path: /docs/reference/functions/graphcool-lib
layout: REFERENCE
beta: true
description: Graphcool Functions are used to add different capabilities to your Graphcool project. Validate mutation input, extend your schema and more!
tags:
  - functions
related:
  further:
  more:
---

# graphcool-lib

The `graphcool-lib` package covers common workflows that occur in Graphcool Functions or other server-side scripts. For a detailed documentation and usage examples, check the [project on GitHub](https://github.com/graphcool/graphcool-lib).

## Usage

The library exposes a helper method `fromEvent` that can be used to initialize a new GraphQL API client that can send queries and mutations and returns a promise.

Typically, all Graphcool Functions expose the `event` object needed for the initialization of `graphcool-lib`, but here is an example how to construct it yourself:

```js
const { fromEvent } = require('graphcool-lib')

const pat = '__PAT__'
const projectId = 'cixne4sn40c7m0122h8fabni1'

const event = {
  context: {
    graphcool: {
      projectId,
      // include a PAT if you need full read/write access on the server-side
      // pat,
    }
  }
}

const api = fromEvent(event).api('simple/v1')

const query = `
  query {
    allMovies {
      id
      title
    }
  }
`

api.request(query)
  .then(data => console.log(data))
```

### Passing arguments

```js
api.request(query, arguments)
```

For example:

```js
api.request(`
    query getMovie($genre: String!) {
      Movie(genre: $genre) {
        id,
        title
      }
    }`, { genre })
    .then(result => {
      ...
    })
```
> Note: the `context` property of the exposed `event` object inside a Graphcool Function will include a [Permanent Authentication Token](!alias-eip7ahqu5o) **if it has the same name as the Graphcool Function**. If no such PAT exists, no PAT will be part of the event's context.
