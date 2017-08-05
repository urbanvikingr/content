---
alias: maiv5eekan
path: /docs/faq/graphql-how-to-download-graphql-sdl-schema
layout: FAQ
title: How to download the GraphQL SDL Schema
description: GraphQL servers expose a type safe GraphQL schema. You can download it in SDL syntax and use it with Relay Modern or other tools.
tags:
  - tooling
  - schema
  - queries
  - graphql
related:
  further:
    - teizeit5se
    - ij2choozae
  more:
    - cahzai2eur
    - shoe5xailo
---

# How to download the GraphQL SDL Schema

The GraphQL schema describes the available types in a GraphQL API using the [SDL (schema definition language)](!alias-kr84dktnp0).

## Download a GraphQL Schema

You can use [graphql-cli](https://github.com/graphcool/graphql-cli) to download the complete GraphQL schema of any GraphQL endpoint. Install the tool and download the schema:

```sh
# install via NPM
npm install -g graphql-cli

# Setup your .graphqlconfig file
graphql init

# Download the schema from the server
graphql get-schema
```

This downloads a GraphQL schema in SDL syntax, which is needed for Relay Modern for example. The schema contains **all necessary type information** for Relay Modern and other tooling. It contains available GraphQL queries and mutations, GraphQL types, mutation payloads, input types and more.

## Watch for Changes

You can also listen for changes to your GraphQL schema and continuously update your schema by running:

```sh
graphql get-schema --watch
```
