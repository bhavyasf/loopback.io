---
lang: en
title: 'API docs: core.service'
keywords: LoopBack 4.0, LoopBack 4, Node.js, TypeScript, OpenAPI
sidebar: lb4_sidebar
editurl: https://github.com/loopbackio/loopback-next/tree/master/packages/core
permalink: /doc/en/lb4/apidocs.core.service.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/core](./core.md) &gt; [service](./core.service.md)

## service() function

`@service` injects a service instance that matches the class or interface.

<b>Signature:</b>

```typescript
export declare function service(serviceInterface?: ServiceInterface, metadata?: InjectionMetadata): (target: Object, member: string | undefined, methodDescriptorOrParameterIndex?: number | TypedPropertyDescriptor<any> | undefined) => void;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  serviceInterface | [ServiceInterface](./core.serviceinterface.md) | <p><i>(Optional)</i> Interface for the service. It can be in one of the following forms:</p><p>- A class, such as MyService - A string that identifies the interface, such as <code>'MyService'</code> - A symbol that identifies the interface, such as <code>Symbol('MyService')</code></p><p>If not provided, the value is inferred from the design:type of the parameter or property</p> |
|  metadata | [InjectionMetadata](./context.injectionmetadata.md) | <i>(Optional)</i> |

<b>Returns:</b>

(target: Object, member: string \| undefined, methodDescriptorOrParameterIndex?: number \| TypedPropertyDescriptor&lt;any&gt; \| undefined) =&gt; void

## Example


```ts

const ctx = new Context();
ctx.bind('my-service').toClass(MyService);
ctx.bind('logger').toClass(Logger);

export class MyController {
  constructor(@service(MyService) private myService: MyService) {}

  @service()
  private logger: Logger;
}

ctx.bind('my-controller').toClass(MyController);
await myController = ctx.get<MyController>('my-controller');
```


