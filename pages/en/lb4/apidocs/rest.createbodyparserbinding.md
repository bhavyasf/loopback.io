---
lang: en
title: 'API docs: rest.createbodyparserbinding'
keywords: LoopBack 4.0, LoopBack 4, Node.js, TypeScript, OpenAPI
sidebar: lb4_sidebar
editurl: https://github.com/loopbackio/loopback-next/tree/master/packages/rest
permalink: /doc/en/lb4/apidocs.rest.createbodyparserbinding.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/rest](./rest.md) &gt; [createBodyParserBinding](./rest.createbodyparserbinding.md)

## createBodyParserBinding() function

Create a binding for the given body parser class

<b>Signature:</b>

```typescript
export declare function createBodyParserBinding(parserClass: Constructor<BodyParser>, key?: BindingAddress<BodyParser>): Binding<BodyParser>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  parserClass | [Constructor](./context.constructor.md)<!-- -->&lt;[BodyParser](./rest.bodyparser.md)<!-- -->&gt; | Body parser class |
|  key | [BindingAddress](./context.bindingaddress.md)<!-- -->&lt;[BodyParser](./rest.bodyparser.md)<!-- -->&gt; | <i>(Optional)</i> Optional binding address |

<b>Returns:</b>

[Binding](./context.binding.md)<!-- -->&lt;[BodyParser](./rest.bodyparser.md)<!-- -->&gt;


