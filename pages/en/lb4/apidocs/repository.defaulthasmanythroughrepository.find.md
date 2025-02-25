---
lang: en
title: 'API docs: repository.defaulthasmanythroughrepository.find'
keywords: LoopBack 4.0, LoopBack 4, Node.js, TypeScript, OpenAPI
sidebar: lb4_sidebar
editurl: https://github.com/loopbackio/loopback-next/tree/master/packages/repository
permalink: /doc/en/lb4/apidocs.repository.defaulthasmanythroughrepository.find.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/repository](./repository.md) &gt; [DefaultHasManyThroughRepository](./repository.defaulthasmanythroughrepository.md) &gt; [find](./repository.defaulthasmanythroughrepository.find.md)

## DefaultHasManyThroughRepository.find() method

<b>Signature:</b>

```typescript
find(filter?: Filter<TargetEntity>, options?: Options & {
        throughOptions?: Options & {
            discriminator?: string;
        };
    } & {
        polymorphicType?: string | string[];
    }): Promise<TargetEntity[]>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  filter | [Filter](./filter.filter.md)<!-- -->&lt;TargetEntity&gt; | <i>(Optional)</i> |
|  options | [Options](./repository.options.md) &amp; { throughOptions?: [Options](./repository.options.md) &amp; { discriminator?: string; }; } &amp; { polymorphicType?: string \| string\[\]; } | <i>(Optional)</i> |

<b>Returns:</b>

Promise&lt;TargetEntity\[\]&gt;


