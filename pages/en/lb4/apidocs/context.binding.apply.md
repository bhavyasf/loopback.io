---
lang: en
title: 'API docs: context.binding.apply'
keywords: LoopBack 4.0, LoopBack 4, Node.js, TypeScript, OpenAPI
sidebar: lb4_sidebar
editurl: https://github.com/loopbackio/loopback-next/tree/master/packages/context
permalink: /doc/en/lb4/apidocs.context.binding.apply.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/context](./context.md) &gt; [Binding](./context.binding.md) &gt; [apply](./context.binding.apply.md)

## Binding.apply() method

Apply one or more template functions to set up the binding with scope, tags, and other attributes as a group.

<b>Signature:</b>

```typescript
apply(...templateFns: BindingTemplate<T>[]): this;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  templateFns | [BindingTemplate](./context.bindingtemplate.md)<!-- -->&lt;T&gt;\[\] | One or more functions to configure the binding |

<b>Returns:</b>

this

## Example


```ts
const serverTemplate = (binding: Binding) =>
  binding.inScope(BindingScope.SINGLETON).tag('server');

const serverBinding = new Binding<RestServer>('servers.RestServer1');
serverBinding.apply(serverTemplate);
```


