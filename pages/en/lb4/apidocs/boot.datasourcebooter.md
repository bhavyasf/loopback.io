---
lang: en
title: 'API docs: boot.datasourcebooter'
keywords: LoopBack 4.0, LoopBack 4, Node.js, TypeScript, OpenAPI
sidebar: lb4_sidebar
editurl: https://github.com/loopbackio/loopback-next/tree/master/packages/boot
permalink: /doc/en/lb4/apidocs.boot.datasourcebooter.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/boot](./boot.md) &gt; [DataSourceBooter](./boot.datasourcebooter.md)

## DataSourceBooter class

A class that extends BaseArtifactBooter to boot the 'DataSource' artifact type. Discovered DataSources are bound using `app.dataSource()`<!-- -->.

Supported phases: configure, discover, load

<b>Signature:</b>

```typescript
export declare class DataSourceBooter extends BaseArtifactBooter 
```
<b>Extends:</b> [BaseArtifactBooter](./boot.baseartifactbooter.md)

## Constructors

|  Constructor | Modifiers | Description |
|  --- | --- | --- |
|  [(constructor)(app, projectRoot, datasourceConfig)](./boot.datasourcebooter._constructor_.md) |  | Constructs a new instance of the <code>DataSourceBooter</code> class |

## Properties

|  Property | Modifiers | Type | Description |
|  --- | --- | --- | --- |
|  [app](./boot.datasourcebooter.app.md) |  | [ApplicationWithRepositories](./repository.applicationwithrepositories.md) |  |
|  [datasourceConfig](./boot.datasourcebooter.datasourceconfig.md) |  | [ArtifactOptions](./boot.artifactoptions.md) |  |

## Methods

|  Method | Modifiers | Description |
|  --- | --- | --- |
|  [load()](./boot.datasourcebooter.load.md) |  | Uses super method to get a list of Artifact classes. Boot each file by creating a DataSourceConstructor and binding it to the application class. |


