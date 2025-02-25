---
lang: en
title: 'API docs: metadata.methodparameterdecoratorfactory'
keywords: LoopBack 4.0, LoopBack 4, Node.js, TypeScript, OpenAPI
sidebar: lb4_sidebar
editurl: https://github.com/loopbackio/loopback-next/tree/master/packages/metadata
permalink: /doc/en/lb4/apidocs.metadata.methodparameterdecoratorfactory.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/metadata](./metadata.md) &gt; [MethodParameterDecoratorFactory](./metadata.methodparameterdecoratorfactory.md)

## MethodParameterDecoratorFactory class

Factory for method level parameter decorator.

<b>Signature:</b>

```typescript
export declare class MethodParameterDecoratorFactory<T> extends DecoratorFactory<T, MetadataMap<T[]>, MethodDecorator> 
```
<b>Extends:</b> [DecoratorFactory](./metadata.decoratorfactory.md)<!-- -->&lt;T, [MetadataMap](./metadata.metadatamap.md)<!-- -->&lt;T\[\]&gt;, MethodDecorator&gt;

## Example

For example, the following code uses `@param` to declare two parameters for `greet()`<!-- -->.

```ts
class MyController {
  @param('name') // Parameter 0
  @param('msg')  // Parameter 1
  greet() {}
}
```

## Methods

|  Method | Modifiers | Description |
|  --- | --- | --- |
|  [create()](./metadata.methodparameterdecoratorfactory.create.md) |  |  |
|  [createDecorator(key, spec, options)](./metadata.methodparameterdecoratorfactory.createdecorator.md) | <code>static</code> | Create a method decorator function |
|  [mergeWithInherited(inheritedMetadata, target, methodName, methodDescriptor)](./metadata.methodparameterdecoratorfactory.mergewithinherited.md) | <code>protected</code> |  |
|  [mergeWithOwn(ownMetadata, target, methodName, methodDescriptor)](./metadata.methodparameterdecoratorfactory.mergewithown.md) | <code>protected</code> |  |


