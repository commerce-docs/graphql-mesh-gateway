---
title: encapsulate | API Mesh for Adobe Developer App Builder
description: Learn how to define a schema for a field with the encapsulate transform.
keywords:
  - API Mesh
  - Extensibility
  - GraphQL
  - Integration
  - REST
  - Tools
---

# `encapsulate` transform

The `encapsulate` transform allows you to easily encapsulate a specific schema into a single field under the root type.

For instance, if your handler created a schema like this, named `mySchema`:

```graphql
type Query {
  something: String
}

type Mutation {
  doSomething: String
}
```

The `encapsulate` transform will change your schema to this:

```graphql
type Query {
  mySchema: mySchemaQuery!
}

type Mutation {
  mySchema: mySchemaMutation!
}

type mySchemaQuery {
  something: String
}

type mySchemaMutation {
  doSomething: String
}
```

This transform is useful when you have multiple APIs in your Mesh Gateway and you wish to have it wrapped with a name to better understand where each field is coming from.

## Usage

The following example encapsulates the Adobe Commerce schema into the `AdobeCommerce` field:

```json
{
  "meshConfig": {
    "sources": [
      {
        "name": "AdobeCommerce",
        "handler": {
          "graphql": {
            "endpoint": "https://venia.magento.com/graphql"
          }
        },
        "transforms": [
          {
            "encapsulate": {
              "applyTo": {
                "query": true,
                "mutation": false,
                "subscription": false
              }
            }
          }
        ]
      }
    ]
  }
}
```

## Config API Reference

-  `name` (type: `String`) - (Optional) The name used for grouping under root types
   -  If you do not specify a `name`, the API name will be used.
-  `applyTo` (type: `Object`) - The root operations the `encapsulate` applies to. Unspecified options default to `true`:
   -  `query` (type: `Boolean`)
   -  `mutation` (type: `Boolean`)
   -  `subscription` (type: `Boolean`)
