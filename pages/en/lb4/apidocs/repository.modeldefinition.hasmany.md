---
lang: en
title: 'API docs: repository.modeldefinition.hasmany'
keywords: LoopBack 4.0, LoopBack 4, Node.js, TypeScript, OpenAPI
sidebar: lb4_sidebar
editurl: https://github.com/loopbackio/loopback-next/tree/master/packages/repository
permalink: /doc/en/lb4/apidocs.repository.modeldefinition.hasmany.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/repository](./repository.md) &gt; [ModelDefinition](./repository.modeldefinition.md) &gt; [hasMany](./repository.modeldefinition.hasmany.md)

## ModelDefinition.hasMany() method

Define a new hasMany relation.

<b>Signature:</b>

```typescript
hasMany(name: string, definition: Omit<HasManyDefinition, 'name' | 'type' | 'targetsMany'>): this;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  name | string | The name of the hasMany relation. |
|  definition | Omit&lt;[HasManyDefinition](./repository.hasmanydefinition.md)<!-- -->, 'name' \| 'type' \| 'targetsMany'&gt; | The definition of the hasMany relation. |

<b>Returns:</b>

this


