---
lang: en
title: 'API docs: context.trycatchfinally'
keywords: LoopBack 4.0, LoopBack 4, Node.js, TypeScript, OpenAPI
sidebar: lb4_sidebar
editurl: https://github.com/loopbackio/loopback-next/tree/master/packages/context
permalink: /doc/en/lb4/apidocs.context.trycatchfinally.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/context](./context.md) &gt; [tryCatchFinally](./context.trycatchfinally.md)

## tryCatchFinally() function

Try to run an action that returns a promise or a value with error and final actions to mimic `try {} catch(err) {} finally {}` for a value or promise.

<b>Signature:</b>

```typescript
export declare function tryCatchFinally<T>(action: () => ValueOrPromise<T>, errorAction?: (err: unknown) => T | never, finalAction?: () => void): ValueOrPromise<T>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  action | () =&gt; [ValueOrPromise](./context.valueorpromise.md)<!-- -->&lt;T&gt; | A function that returns a promise or a value |
|  errorAction | (err: unknown) =&gt; T \| never | <i>(Optional)</i> A function to be called once the action is rejected (synchronously or asynchronously). It must either return a new value or throw an error. |
|  finalAction | () =&gt; void | <i>(Optional)</i> A function to be called once the action is fulfilled or rejected (synchronously or asynchronously) |

<b>Returns:</b>

[ValueOrPromise](./context.valueorpromise.md)<!-- -->&lt;T&gt;


