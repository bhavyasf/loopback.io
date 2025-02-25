---
lang: en
title: 'API docs: express.toexpressmiddleware'
keywords: LoopBack 4.0, LoopBack 4, Node.js, TypeScript, OpenAPI
sidebar: lb4_sidebar
editurl: https://github.com/loopbackio/loopback-next/tree/master/packages/express
permalink: /doc/en/lb4/apidocs.express.toexpressmiddleware.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/express](./express.md) &gt; [toExpressMiddleware](./express.toexpressmiddleware.md)

## toExpressMiddleware() function

An adapter function to create an Express middleware handler to discover and invoke registered LoopBack-style middleware in the context.

<b>Signature:</b>

```typescript
export declare function toExpressMiddleware(ctx: Context): ExpressRequestHandler;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  ctx | [Context](./context.context.md) | Context object to discover registered middleware |

<b>Returns:</b>

[ExpressRequestHandler](./express.expressrequesthandler.md)


