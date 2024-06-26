---
title: API Mesh for Adobe Developer App Builder Overview
description: Learn how API Mesh for Adobe Developer App Builder enables you to route incoming requests from customers to different underlying remote services.
keywords:
  - API Mesh
  - Extensibility
  - GraphQL
  - Integration
  - REST
  - Tools
---

# What is API Mesh for Adobe Developer App Builder?

API Mesh enables developers to integrate third-party APIs with other Adobe products, like App Builder, Adobe IO Gateway, or other serverless technologies.

By integrating multiple APIs, developers can allow these external systems to synchronize data, and participate in distributed workflows.

API Mesh allows developers to configure multiple APIs and other sources and serve them through a gateway. Developers can query the combined sources through a single [GraphQL] query.

## Features

-  **API Mesh** - A reverse proxy that accepts most API calls for many backend services
-  **Configurable Integrations** - Low/No-code method to integrate with your own private APIs with Adobe Commerce and other Adobe products, and third-party APIs
-  **Backwards Compatibility** - Preserve existing APIs while gradually adopting new ones
-  **Extensibility** - Customize and extend all of your APIs directly in the gateway without making changes to the API source

## Where to go next

-  [Getting started]
   -  [Prerequisites]
   -  [Create an Adobe IO account]
   -  [Configure your environment]
-  [Create a mesh]

## Benefits of using GraphQL

<InlineAlert variant="info" slots="text"/>

[GraphQL] is a query language for your API that lets you query exactly the information you need and only the information you need. [GraphQL Mesh] allows you to use GraphQL to query multiple data sources simultaneously.

[GraphQL] has several advantages over REST and other APIs:

-  **GraphQL has predictable responses**: With GraphQL, you specify what information your response should contain.
-  **Faster response time**: Since you can control what data appears in your response, there is less extraneous data slowing down your calls.
-  **Defined Schema**: With its well-defined set of types, GraphQL lets you know what data you can query.

<!-- Link Definitions -->
[supports GraphQL queries]: https://devdocs.magento.com/guides/v2.4/graphql/index.html
[GraphQL]: https://graphql.org/
[GraphQL Mesh]: https://www.graphql-mesh.com/
[Getting started]: getting-started.md
[Prerequisites]: getting-started.md#Prerequisites
[Create an Adobe IO account]: getting-started.md#prerequisites
[Configure your environment]: getting-started.md#configure-your-environment
[Create a mesh]: create-mesh.md
