---
lang: en
title: 'API docs: openapi-v3.param.array'
keywords: LoopBack 4.0, LoopBack 4, Node.js, TypeScript, OpenAPI
sidebar: lb4_sidebar
editurl: https://github.com/loopbackio/loopback-next/tree/master/packages/openapi-v3
permalink: /doc/en/lb4/apidocs.openapi-v3.param.array.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/openapi-v3](./openapi-v3.md) &gt; [param](./openapi-v3.param.md) &gt; [array](./openapi-v3.param.array.md)

## param.array variable

Define a parameter of `array` type.

<b>Signature:</b>

```typescript
array: (name: string, source: ParameterLocation, itemSpec: SchemaObject | ReferenceObject) => (target: object, member: string, index: number) => void
```

## Example


```ts
export class MyController {
  @get('/greet')
  greet(@param.array('names', 'query', {type: 'string'}) names: string[]): string {
    return `Hello, ${names}`;
  }
}
```


