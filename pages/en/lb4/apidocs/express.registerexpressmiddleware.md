---
lang: en
title: 'API docs: express.registerexpressmiddleware'
keywords: LoopBack 4.0, LoopBack 4, Node.js, TypeScript, OpenAPI
sidebar: lb4_sidebar
editurl: https://github.com/loopbackio/loopback-next/tree/master/packages/express
permalink: /doc/en/lb4/apidocs.express.registerexpressmiddleware.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/express](./express.md) &gt; [registerExpressMiddleware](./express.registerexpressmiddleware.md)

## registerExpressMiddleware() function

Bind a Express middleware to the given context

<b>Signature:</b>

```typescript
export declare function registerExpressMiddleware<CFG>(ctx: Context, middlewareFactory: ExpressMiddlewareFactory<CFG>, middlewareConfig?: CFG, options?: MiddlewareBindingOptions): Binding<Middleware>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  ctx | [Context](./context.context.md) | Context object |
|  middlewareFactory | [ExpressMiddlewareFactory](./express.expressmiddlewarefactory.md)<!-- -->&lt;CFG&gt; | Middleware module name or factory function |
|  middlewareConfig | CFG | <i>(Optional)</i> Middleware config |
|  options | [MiddlewareBindingOptions](./express.middlewarebindingoptions.md) | <i>(Optional)</i> Options for registration |

<b>Returns:</b>

[Binding](./context.binding.md)<!-- -->&lt;[Middleware](./express.middleware.md)<!-- -->&gt;


