---
alias: aeghee3di9
path: /blog/2017-08-01-graphql-config-and-cli
layout: BLOG
description: Improving GraphQL tooling with a unified configuration format and the graphql-cli to support local development workflows.
preview: preview.png
publication_date: '2017-08-01'
tags:
  - graphql
  - open-source
  - graphql-cli
  - graphql-config
related:
  further:
  more:
---

# New Tooling to Improve Your GraphQL Workflows

Together with many awesome contributors from the community including the GraphQL team at Facebook, we have developed [`graphql-config`](https://github.com/graphcool/graphql-config) - a unified way to configure GraphQL projects. We're also excited to present the beta version of a new command-line tool to improve your local GraphQL development workflow: [`graphql-cli`](https://github.com/graphcool/graphql-cli). 

## Fragmentation in GraphQL Tooling

Despite being a relatively young technology, GraphQL already has seen a great amount of adoption. With the growing number of projects that are using GraphQL, it gets more and more important for the community to develop standards and unify solutions to common problems that developers encounter in GraphQL projects.

One of these problems is the question [how to write configuration files](https://github.com/graphcool/graphql-config/issues/16) in a way that *all* dependent tools can understand them. 

If you've already worked on a larger GraphQL project, chances are you had to configure some of your tooling with information about your GraphQL schema. Just taking three popular tools as an example, all of them are using different configuration formats to specify where your schema is located:

* For [eslint-plugin-graphql](https://medium.com/r/?url=https%3A%2F%2Fgithub.com%2Fapollostack%2Feslint-plugin-graphql), you need to reference your schema from  `.eslintrc`
* [GraphQL Language services](https://medium.com/r/?url=https%3A%2F%2Fgithub.com%2Fgraphql%2Fgraphql-language-service) uses its own custom config format
* [`js-graphql-intellij-plugin`](https://medium.com/r/?url=https%3A%2F%2Fgithub.com%2Fjimkyndemeyer%2Fjs-graphql-intellij-plugin) uses another custom config format

With the growing number of tools relying on the schema, more and more different configuration files and formats are needed. The problem of fragmented configuration gets even more complex with more specific use cases, like using different environments for dev and production or adding additional endpoints for [subscription](https://www.graph.cool/docs/reference/simple-api/subscriptions-aip7oojeiv/) servers.

The solution? There needs to be a standard for how to configure GraphQL projects.

![](./standards.png)

## `.graphqlconfig` - One Config to Rule Them All

The format specified by [`graphql-config`](https://github.com/graphcool/graphql-config)  will be the foundation for all schema-aware GraphQL tools. Here's a minimal example of what a `.graphqlconfig` can look like given a [SDL](https://www.graph.cool/docs/faq/graphql-sdl-schema-definition-language-kr84dktnp0/)-based schema file:

```js
{
  "schemaPath": "./schema.graphql"
}
```

Note that the referenced schema file might as well be in JSON format (as would be the case if it was generated based on the [introspection](https://www.graph.cool/docs/faq/graphql-introspection-queries-shoe5xailo/) dump from the GraphQL server).

In more complex setups, you might want to configure additional endpoints for multiple environments or for a subscription server:

```js
{
  "schemaPath": "schema.graphql",
  "extensions": {
    "endpoints": {
      "prod": {
        "url": "https://api.graph.cool/graphql",
        "subscription": {
          "url": "wss://subscriptions.graph.cool"
        }
      },
      "dev": {
        "url": "https://localhost:3000/graphql",
        "subscription": {
          "url": "wss://localhost:3001"
        }
      },
    }
  }
}
```

For a complete overview of the different options that can be used in a `.graphqlconfig`, you can refer to the full [specification](https://github.com/graphcool/graphql-config/blob/master/specification.md#use-cases). 


## `graphql-cli` - The Swiss Army Knife for your GraphQL Project

Along with the unified way to write configuration files, we're also introducing a command-line tool to improve your local GraphQL development workflow: [`graphql-cli`](https://github.com/graphcool/graphql-cli).

You can use it to quickly download the schema from a specific endpoint, open a GraphQL playground or show the schema diff between two different environments. Here is the CLI in action:

![](./demo.gif)

You can simply install the CLI using npm:

```bash
npm install -g graphql-cli
```

The CLI ships with a plugin system so you can easily add commands to match your development workflow. You can for example check out the [GraphQL Voyager plugin](https://github.com/graphcool/graphql-cli-voyager).


## Continuously Improving Developer Experience

With a unified format to write GraphQL configuration files as well as a CLI that supports common development workflows, the GraphQL tooling space sees two major additions. These are going to improve developer experience and lay the foundation for better interoperability of relevant tools in the future.

### Get Involved

`graphql-config` and the `graphql-cli` are both community projects and as such will provide the most value if many people collaborate on them!

**If you're the author or maintainer of a GraphQL library or another related tool, we encourage you to adopt the `graphql-config` standard.** Please link to this [GitHub issue](https://github.com/graphcool/graphql-config/issues/27) to track the progress. 

As mentioned before, the `graphql-cli` can be extended with plugins to support custom use cases. **Feel free to start building your own plugins to support your GraphQL development workflow or tackle further use cases.** Ideas for more features could be plugins for code generation or letting people quickly spin up their own GraphQL server with `graphql-up`. We're excited to see what you're going to build!
