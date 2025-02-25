---
lang: en
title: 'API docs: repository.repositorymixin'
keywords: LoopBack 4.0, LoopBack 4, Node.js, TypeScript, OpenAPI
sidebar: lb4_sidebar
editurl: https://github.com/loopbackio/loopback-next/tree/master/packages/repository
permalink: /doc/en/lb4/apidocs.repository.repositorymixin.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/repository](./repository.md) &gt; [RepositoryMixin](./repository.repositorymixin.md)

## RepositoryMixin() function

A mixin class for Application that creates a .repository() function to register a repository automatically. Also overrides component function to allow it to register repositories automatically.

<b>Signature:</b>

```typescript
export declare function RepositoryMixin<T extends MixinTarget<Application>>(superClass: T): {
    new (...args: any[]): {
        repository<R extends Repository<any>>(repoClass: Class<R>, nameOrOptions?: string | BindingFromClassOptions): Binding<R>;
        getRepository<R_1 extends Repository<any>>(repo: Class<R_1>): Promise<R_1>;
        dataSource<D extends juggler.DataSource>(dataSource: D | Class<D>, nameOrOptions?: string | BindingFromClassOptions): Binding<D>;
        model<M extends Class<unknown>>(modelClass: M): Binding<M>;
        component<C extends Component = Component>(componentCtor: Constructor<C>, nameOrOptions?: string | BindingFromClassOptions): Binding<C>;
        mountComponentRepositories(componentInstanceOrClass: Class<unknown> | RepositoryComponent): void;
        mountComponentModels(component: RepositoryComponent): void;
        migrateSchema(options?: SchemaMigrationOptions): Promise<void>;
        readonly options: import("@loopback/core").ApplicationConfig;
        readonly state: string;
        controller: <T_1>(controllerCtor: import("@loopback/core").ControllerClass<T_1>, nameOrOptions?: string | BindingFromClassOptions | undefined) => Binding<T_1>;
        server: <T_2 extends import("@loopback/core").Server>(ctor: Constructor<T_2>, nameOrOptions?: string | BindingFromClassOptions | undefined) => Binding<T_2>;
        servers: <T_3 extends import("@loopback/core").Server>(ctors: Constructor<T_3>[]) => Binding<any>[];
        getServer: <T_4 extends import("@loopback/core").Server>(target: string | Constructor<T_4>) => Promise<T_4>;
        init: () => Promise<void>;
        onInit: (fn: () => import("@loopback/core").ValueOrPromise<void>) => Binding<import("@loopback/core").LifeCycleObserver>;
        start: () => Promise<void>;
        onStart: (fn: () => import("@loopback/core").ValueOrPromise<void>) => Binding<import("@loopback/core").LifeCycleObserver>;
        stop: () => Promise<void>;
        onStop: (fn: () => import("@loopback/core").ValueOrPromise<void>) => Binding<import("@loopback/core").LifeCycleObserver>;
        setMetadata: (metadata: import("@loopback/core").ApplicationMetadata) => void;
        lifeCycleObserver: <T_5 extends import("@loopback/core").LifeCycleObserver>(ctor: Constructor<T_5>, nameOrOptions?: string | BindingFromClassOptions | undefined) => Binding<T_5>;
        service: <S>(cls: import("@loopback/core").ServiceOrProviderClass<S>, nameOrOptions?: string | import("@loopback/core").ServiceOptions | undefined) => Binding<S>;
        interceptor: (interceptor: import("@loopback/core").Interceptor | Constructor<import("@loopback/core").Provider<import("@loopback/core").Interceptor>>, nameOrOptions?: string | import("@loopback/core").InterceptorBindingOptions | undefined) => Binding<import("@loopback/core").Interceptor>;
        readonly name: string;
        readonly subscriptionManager: import("@loopback/core").ContextSubscriptionManager;
        scope: BindingScope;
        readonly parent: import("@loopback/core").Context | undefined;
        emitEvent: <T_6 extends import("@loopback/core").ContextEvent>(type: string, event: T_6) => void;
        emitError: (err: unknown) => void;
        bind: <ValueType = any>(key: import("@loopback/core").BindingAddress<ValueType>) => Binding<ValueType>;
        add: (binding: Binding<unknown>) => Application;
        configure: <ConfigValueType = any>(key?: import("@loopback/core").BindingAddress<unknown> | undefined) => Binding<ConfigValueType>;
        getConfigAsValueOrPromise: <ConfigValueType_1>(key: import("@loopback/core").BindingAddress<unknown>, propertyPath?: string | undefined, resolutionOptions?: import("@loopback/core").ResolutionOptions | undefined) => import("@loopback/core").ValueOrPromise<ConfigValueType_1 | undefined>;
        getConfig: <ConfigValueType_2>(key: import("@loopback/core").BindingAddress<unknown>, propertyPath?: string | undefined, resolutionOptions?: import("@loopback/core").ResolutionOptions | undefined) => Promise<ConfigValueType_2 | undefined>;
        getConfigSync: <ConfigValueType_3>(key: import("@loopback/core").BindingAddress<unknown>, propertyPath?: string | undefined, resolutionOptions?: import("@loopback/core").ResolutionOptions | undefined) => ConfigValueType_3 | undefined;
        unbind: (key: import("@loopback/core").BindingAddress<unknown>) => boolean;
        subscribe: (observer: import("@loopback/core").ContextEventObserver) => import("@loopback/core").Subscription;
        unsubscribe: (observer: import("@loopback/core").ContextEventObserver) => boolean;
        close: () => void;
        isSubscribed: (observer: import("@loopback/core").ContextObserver) => boolean;
        createView: <T_7 = unknown>(filter: import("@loopback/core").BindingFilter, comparator?: import("@loopback/core").BindingComparator | undefined, options?: Omit<import("@loopback/core").ResolutionOptions, "session"> | undefined) => import("@loopback/core").ContextView<T_7>;
        contains: (key: import("@loopback/core").BindingAddress<unknown>) => boolean;
        isBound: (key: import("@loopback/core").BindingAddress<unknown>) => boolean;
        getOwnerContext: (keyOrBinding: import("@loopback/core").BindingAddress<unknown> | Readonly<Binding<unknown>>) => import("@loopback/core").Context | undefined;
        getScopedContext: (scope: BindingScope.APPLICATION | BindingScope.SERVER | BindingScope.REQUEST) => import("@loopback/core").Context | undefined;
        getResolutionContext: (binding: Readonly<Binding<unknown>>) => import("@loopback/core").Context | undefined;
        isVisibleTo: (ctx: import("@loopback/core").Context) => boolean;
        find: <ValueType_1 = any>(pattern?: string | RegExp | import("@loopback/core").BindingFilter | undefined) => Readonly<Binding<ValueType_1>>[];
        findByTag: <ValueType_2 = any>(tagFilter: RegExp | import("@loopback/core").BindingTag) => Readonly<Binding<ValueType_2>>[];
        get: {
            <ValueType_3>(keyWithPath: import("@loopback/core").BindingAddress<ValueType_3>, session?: import("@loopback/core").ResolutionSession | undefined): Promise<ValueType_3>;
            <ValueType_4>(keyWithPath: import("@loopback/core").BindingAddress<ValueType_4>, options: import("@loopback/core").ResolutionOptions): Promise<ValueType_4 | undefined>;
        };
        getSync: {
            <ValueType_5>(keyWithPath: import("@loopback/core").BindingAddress<ValueType_5>, session?: import("@loopback/core").ResolutionSession | undefined): ValueType_5;
            <ValueType_6>(keyWithPath: import("@loopback/core").BindingAddress<ValueType_6>, options?: import("@loopback/core").ResolutionOptions | undefined): ValueType_6 | undefined;
        };
        getBinding: {
            <ValueType_7 = any>(key: import("@loopback/core").BindingAddress<ValueType_7>): Binding<ValueType_7>;
            <ValueType_8>(key: import("@loopback/core").BindingAddress<ValueType_8>, options?: {
                optional?: boolean | undefined;
            } | undefined): Binding<ValueType_8> | undefined;
        };
        findOrCreateBinding: <T_8>(key: import("@loopback/core").BindingAddress<T_8>, policy?: import("@loopback/core").BindingCreationPolicy | undefined) => Binding<T_8>;
        getValueOrPromise: <ValueType_9>(keyWithPath: import("@loopback/core").BindingAddress<ValueType_9>, optionsOrSession?: import("@loopback/core").ResolutionOptionsOrSession | undefined) => import("@loopback/core").ValueOrPromise<ValueType_9 | undefined>;
        toJSON: () => import("@loopback/core").JSONObject;
        inspect: (options?: import("@loopback/core").ContextInspectOptions | undefined) => import("@loopback/core").JSONObject;
        on: {
            (eventName: "bind" | "unbind", listener: import("@loopback/core").ContextEventListener): Application;
            (event: string | symbol, listener: (...args: any[]) => void): Application;
        };
        once: {
            (eventName: "bind" | "unbind", listener: import("@loopback/core").ContextEventListener): Application;
            (event: string | symbol, listener: (...args: any[]) => void): Application;
        };
        addListener: (event: string | symbol, listener: (...args: any[]) => void) => Application;
        removeListener: (event: string | symbol, listener: (...args: any[]) => void) => Application;
        off: (event: string | symbol, listener: (...args: any[]) => void) => Application;
        removeAllListeners: (event?: string | symbol | undefined) => Application;
        setMaxListeners: (n: number) => Application;
        getMaxListeners: () => number;
        listeners: (event: string | symbol) => Function[];
        rawListeners: (event: string | symbol) => Function[];
        emit: (event: string | symbol, ...args: any[]) => boolean;
        listenerCount: (event: string | symbol) => number;
        prependListener: (event: string | symbol, listener: (...args: any[]) => void) => Application;
        prependOnceListener: (event: string | symbol, listener: (...args: any[]) => void) => Application;
        eventNames: () => (string | symbol)[];
    };
} & T;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  superClass | T | Application class |

<b>Returns:</b>

{ new (...args: any\[\]): { repository&lt;R extends [Repository](./repository.repository.md)<!-- -->&lt;any&gt;&gt;(repoClass: [Class](./repository.class.md)<!-- -->&lt;R&gt;, nameOrOptions?: string \| [BindingFromClassOptions](./context.bindingfromclassoptions.md)<!-- -->): [Binding](./context.binding.md)<!-- -->&lt;R&gt;; getRepository&lt;R\_1 extends [Repository](./repository.repository.md)<!-- -->&lt;any&gt;&gt;(repo: [Class](./repository.class.md)<!-- -->&lt;R\_1&gt;): Promise&lt;R\_1&gt;; dataSource&lt;D extends juggler.DataSource&gt;(dataSource: D \| [Class](./repository.class.md)<!-- -->&lt;D&gt;, nameOrOptions?: string \| [BindingFromClassOptions](./context.bindingfromclassoptions.md)<!-- -->): [Binding](./context.binding.md)<!-- -->&lt;D&gt;; model&lt;M extends [Class](./repository.class.md)<!-- -->&lt;unknown&gt;&gt;(modelClass: M): [Binding](./context.binding.md)<!-- -->&lt;M&gt;; component&lt;C extends [Component](./core.component.md) = [Component](./core.component.md)<!-- -->&gt;(componentCtor: [Constructor](./context.constructor.md)<!-- -->&lt;C&gt;, nameOrOptions?: string \| [BindingFromClassOptions](./context.bindingfromclassoptions.md)<!-- -->): [Binding](./context.binding.md)<!-- -->&lt;C&gt;; mountComponentRepositories(componentInstanceOrClass: [Class](./repository.class.md)<!-- -->&lt;unknown&gt; \| [RepositoryComponent](./repository.repositorycomponent.md)<!-- -->): void; mountComponentModels(component: [RepositoryComponent](./repository.repositorycomponent.md)<!-- -->): void; migrateSchema(options?: [SchemaMigrationOptions](./repository.schemamigrationoptions.md)<!-- -->): Promise&lt;void&gt;; readonly options: import("@loopback/core").[ApplicationConfig](./core.applicationconfig.md)<!-- -->; readonly state: string; controller: &lt;T\_1&gt;(controllerCtor: import("@loopback/core").[ControllerClass](./core.controllerclass.md)<!-- -->&lt;T\_1&gt;, nameOrOptions?: string \| [BindingFromClassOptions](./context.bindingfromclassoptions.md) \| undefined) =&gt; [Binding](./context.binding.md)<!-- -->&lt;T\_1&gt;; server: &lt;T\_2 extends import("@loopback/core").[Server](./core.server.md)<!-- -->&gt;(ctor: [Constructor](./context.constructor.md)<!-- -->&lt;T\_2&gt;, nameOrOptions?: string \| [BindingFromClassOptions](./context.bindingfromclassoptions.md) \| undefined) =&gt; [Binding](./context.binding.md)<!-- -->&lt;T\_2&gt;; servers: &lt;T\_3 extends import("@loopback/core").[Server](./core.server.md)<!-- -->&gt;(ctors: [Constructor](./context.constructor.md)<!-- -->&lt;T\_3&gt;\[\]) =&gt; [Binding](./context.binding.md)<!-- -->&lt;any&gt;\[\]; getServer: &lt;T\_4 extends import("@loopback/core").[Server](./core.server.md)<!-- -->&gt;(target: string \| [Constructor](./context.constructor.md)<!-- -->&lt;T\_4&gt;) =&gt; Promise&lt;T\_4&gt;; init: () =&gt; Promise&lt;void&gt;; onInit: (fn: () =&gt; import("@loopback/core").[ValueOrPromise](./context.valueorpromise.md)<!-- -->&lt;void&gt;) =&gt; [Binding](./context.binding.md)<!-- -->&lt;import("@loopback/core").[LifeCycleObserver](./core.lifecycleobserver.md)<!-- -->&gt;; start: () =&gt; Promise&lt;void&gt;; onStart: (fn: () =&gt; import("@loopback/core").[ValueOrPromise](./context.valueorpromise.md)<!-- -->&lt;void&gt;) =&gt; [Binding](./context.binding.md)<!-- -->&lt;import("@loopback/core").[LifeCycleObserver](./core.lifecycleobserver.md)<!-- -->&gt;; stop: () =&gt; Promise&lt;void&gt;; onStop: (fn: () =&gt; import("@loopback/core").[ValueOrPromise](./context.valueorpromise.md)<!-- -->&lt;void&gt;) =&gt; [Binding](./context.binding.md)<!-- -->&lt;import("@loopback/core").[LifeCycleObserver](./core.lifecycleobserver.md)<!-- -->&gt;; setMetadata: (metadata: import("@loopback/core").[ApplicationMetadata](./core.applicationmetadata.md)<!-- -->) =&gt; void; lifeCycleObserver: &lt;T\_5 extends import("@loopback/core").[LifeCycleObserver](./core.lifecycleobserver.md)<!-- -->&gt;(ctor: [Constructor](./context.constructor.md)<!-- -->&lt;T\_5&gt;, nameOrOptions?: string \| [BindingFromClassOptions](./context.bindingfromclassoptions.md) \| undefined) =&gt; [Binding](./context.binding.md)<!-- -->&lt;T\_5&gt;; service: &lt;S&gt;(cls: import("@loopback/core").[ServiceOrProviderClass](./core.serviceorproviderclass.md)<!-- -->&lt;S&gt;, nameOrOptions?: string \| import("@loopback/core").[ServiceOptions](./core.serviceoptions.md) \| undefined) =&gt; [Binding](./context.binding.md)<!-- -->&lt;S&gt;; interceptor: (interceptor: import("@loopback/core").[Interceptor](./context.interceptor.md) \| [Constructor](./context.constructor.md)<!-- -->&lt;import("@loopback/core").[Provider](./context.provider.md)<!-- -->&lt;import("@loopback/core").[Interceptor](./context.interceptor.md)<!-- -->&gt;&gt;, nameOrOptions?: string \| import("@loopback/core").[InterceptorBindingOptions](./context.interceptorbindingoptions.md) \| undefined) =&gt; [Binding](./context.binding.md)<!-- -->&lt;import("@loopback/core").[Interceptor](./context.interceptor.md)<!-- -->&gt;; readonly name: string; readonly subscriptionManager: import("@loopback/core").[ContextSubscriptionManager](./context.contextsubscriptionmanager.md)<!-- -->; scope: [BindingScope](./context.bindingscope.md)<!-- -->; readonly parent: import("@loopback/core").[Context](./context.context.md) \| undefined; emitEvent: &lt;T\_6 extends import("@loopback/core").[ContextEvent](./context.contextevent.md)<!-- -->&gt;(type: string, event: T\_6) =&gt; void; emitError: (err: unknown) =&gt; void; bind: &lt;ValueType = any&gt;(key: import("@loopback/core").[BindingAddress](./context.bindingaddress.md)<!-- -->&lt;ValueType&gt;) =&gt; [Binding](./context.binding.md)<!-- -->&lt;ValueType&gt;; add: (binding: [Binding](./context.binding.md)<!-- -->&lt;unknown&gt;) =&gt; [Application](./core.application.md)<!-- -->; configure: &lt;ConfigValueType = any&gt;(key?: import("@loopback/core").[BindingAddress](./context.bindingaddress.md)<!-- -->&lt;unknown&gt; \| undefined) =&gt; [Binding](./context.binding.md)<!-- -->&lt;ConfigValueType&gt;; getConfigAsValueOrPromise: &lt;ConfigValueType\_1&gt;(key: import("@loopback/core").[BindingAddress](./context.bindingaddress.md)<!-- -->&lt;unknown&gt;, propertyPath?: string \| undefined, resolutionOptions?: import("@loopback/core").[ResolutionOptions](./context.resolutionoptions.md) \| undefined) =&gt; import("@loopback/core").[ValueOrPromise](./context.valueorpromise.md)<!-- -->&lt;ConfigValueType\_1 \| undefined&gt;; getConfig: &lt;ConfigValueType\_2&gt;(key: import("@loopback/core").[BindingAddress](./context.bindingaddress.md)<!-- -->&lt;unknown&gt;, propertyPath?: string \| undefined, resolutionOptions?: import("@loopback/core").[ResolutionOptions](./context.resolutionoptions.md) \| undefined) =&gt; Promise&lt;ConfigValueType\_2 \| undefined&gt;; getConfigSync: &lt;ConfigValueType\_3&gt;(key: import("@loopback/core").[BindingAddress](./context.bindingaddress.md)<!-- -->&lt;unknown&gt;, propertyPath?: string \| undefined, resolutionOptions?: import("@loopback/core").[ResolutionOptions](./context.resolutionoptions.md) \| undefined) =&gt; ConfigValueType\_3 \| undefined; unbind: (key: import("@loopback/core").[BindingAddress](./context.bindingaddress.md)<!-- -->&lt;unknown&gt;) =&gt; boolean; subscribe: (observer: import("@loopback/core").[ContextEventObserver](./context.contexteventobserver.md)<!-- -->) =&gt; import("@loopback/core").[Subscription](./context.subscription.md)<!-- -->; unsubscribe: (observer: import("@loopback/core").[ContextEventObserver](./context.contexteventobserver.md)<!-- -->) =&gt; boolean; close: () =&gt; void; isSubscribed: (observer: import("@loopback/core").[ContextObserver](./context.contextobserver.md)<!-- -->) =&gt; boolean; createView: &lt;T\_7 = unknown&gt;(filter: import("@loopback/core").[BindingFilter](./context.bindingfilter.md)<!-- -->, comparator?: import("@loopback/core").[BindingComparator](./context.bindingcomparator.md) \| undefined, options?: Omit&lt;import("@loopback/core").[ResolutionOptions](./context.resolutionoptions.md)<!-- -->, "session"&gt; \| undefined) =&gt; import("@loopback/core").[ContextView](./context.contextview.md)<!-- -->&lt;T\_7&gt;; contains: (key: import("@loopback/core").[BindingAddress](./context.bindingaddress.md)<!-- -->&lt;unknown&gt;) =&gt; boolean; isBound: (key: import("@loopback/core").[BindingAddress](./context.bindingaddress.md)<!-- -->&lt;unknown&gt;) =&gt; boolean; getOwnerContext: (keyOrBinding: import("@loopback/core").[BindingAddress](./context.bindingaddress.md)<!-- -->&lt;unknown&gt; \| Readonly&lt;[Binding](./context.binding.md)<!-- -->&lt;unknown&gt;&gt;) =&gt; import("@loopback/core").[Context](./context.context.md) \| undefined; getScopedContext: (scope: [BindingScope.APPLICATION](./context.bindingscope.md) \| [BindingScope.SERVER](./context.bindingscope.md) \| [BindingScope.REQUEST](./context.bindingscope.md)<!-- -->) =&gt; import("@loopback/core").[Context](./context.context.md) \| undefined; getResolutionContext: (binding: Readonly&lt;[Binding](./context.binding.md)<!-- -->&lt;unknown&gt;&gt;) =&gt; import("@loopback/core").[Context](./context.context.md) \| undefined; isVisibleTo: (ctx: import("@loopback/core").[Context](./context.context.md)<!-- -->) =&gt; boolean; find: &lt;ValueType\_1 = any&gt;(pattern?: string \| RegExp \| import("@loopback/core").[BindingFilter](./context.bindingfilter.md) \| undefined) =&gt; Readonly&lt;[Binding](./context.binding.md)<!-- -->&lt;ValueType\_1&gt;&gt;\[\]; findByTag: &lt;ValueType\_2 = any&gt;(tagFilter: RegExp \| import("@loopback/core").[BindingTag](./context.bindingtag.md)<!-- -->) =&gt; Readonly&lt;[Binding](./context.binding.md)<!-- -->&lt;ValueType\_2&gt;&gt;\[\]; get: { &lt;ValueType\_3&gt;(keyWithPath: import("@loopback/core").[BindingAddress](./context.bindingaddress.md)<!-- -->&lt;ValueType\_3&gt;, session?: import("@loopback/core").[ResolutionSession](./context.resolutionsession.md) \| undefined): Promise&lt;ValueType\_3&gt;; &lt;ValueType\_4&gt;(keyWithPath: import("@loopback/core").[BindingAddress](./context.bindingaddress.md)<!-- -->&lt;ValueType\_4&gt;, options: import("@loopback/core").[ResolutionOptions](./context.resolutionoptions.md)<!-- -->): Promise&lt;ValueType\_4 \| undefined&gt;; }; getSync: { &lt;ValueType\_5&gt;(keyWithPath: import("@loopback/core").[BindingAddress](./context.bindingaddress.md)<!-- -->&lt;ValueType\_5&gt;, session?: import("@loopback/core").[ResolutionSession](./context.resolutionsession.md) \| undefined): ValueType\_5; &lt;ValueType\_6&gt;(keyWithPath: import("@loopback/core").[BindingAddress](./context.bindingaddress.md)<!-- -->&lt;ValueType\_6&gt;, options?: import("@loopback/core").[ResolutionOptions](./context.resolutionoptions.md) \| undefined): ValueType\_6 \| undefined; }; getBinding: { &lt;ValueType\_7 = any&gt;(key: import("@loopback/core").[BindingAddress](./context.bindingaddress.md)<!-- -->&lt;ValueType\_7&gt;): [Binding](./context.binding.md)<!-- -->&lt;ValueType\_7&gt;; &lt;ValueType\_8&gt;(key: import("@loopback/core").[BindingAddress](./context.bindingaddress.md)<!-- -->&lt;ValueType\_8&gt;, options?: { optional?: boolean \| undefined; } \| undefined): [Binding](./context.binding.md)<!-- -->&lt;ValueType\_8&gt; \| undefined; }; findOrCreateBinding: &lt;T\_8&gt;(key: import("@loopback/core").[BindingAddress](./context.bindingaddress.md)<!-- -->&lt;T\_8&gt;, policy?: import("@loopback/core").[BindingCreationPolicy](./context.bindingcreationpolicy.md) \| undefined) =&gt; [Binding](./context.binding.md)<!-- -->&lt;T\_8&gt;; getValueOrPromise: &lt;ValueType\_9&gt;(keyWithPath: import("@loopback/core").[BindingAddress](./context.bindingaddress.md)<!-- -->&lt;ValueType\_9&gt;, optionsOrSession?: import("@loopback/core").[ResolutionOptionsOrSession](./context.resolutionoptionsorsession.md) \| undefined) =&gt; import("@loopback/core").[ValueOrPromise](./context.valueorpromise.md)<!-- -->&lt;ValueType\_9 \| undefined&gt;; toJSON: () =&gt; import("@loopback/core").[JSONObject](./context.jsonobject.md)<!-- -->; inspect: (options?: import("@loopback/core").[ContextInspectOptions](./context.contextinspectoptions.md) \| undefined) =&gt; import("@loopback/core").[JSONObject](./context.jsonobject.md)<!-- -->; on: { (eventName: "bind" \| "unbind", listener: import("@loopback/core").[ContextEventListener](./context.contexteventlistener.md)<!-- -->): [Application](./core.application.md)<!-- -->; (event: string \| symbol, listener: (...args: any\[\]) =&gt; void): [Application](./core.application.md)<!-- -->; }; once: { (eventName: "bind" \| "unbind", listener: import("@loopback/core").[ContextEventListener](./context.contexteventlistener.md)<!-- -->): [Application](./core.application.md)<!-- -->; (event: string \| symbol, listener: (...args: any\[\]) =&gt; void): [Application](./core.application.md)<!-- -->; }; addListener: (event: string \| symbol, listener: (...args: any\[\]) =&gt; void) =&gt; [Application](./core.application.md)<!-- -->; removeListener: (event: string \| symbol, listener: (...args: any\[\]) =&gt; void) =&gt; [Application](./core.application.md)<!-- -->; off: (event: string \| symbol, listener: (...args: any\[\]) =&gt; void) =&gt; [Application](./core.application.md)<!-- -->; removeAllListeners: (event?: string \| symbol \| undefined) =&gt; [Application](./core.application.md)<!-- -->; setMaxListeners: (n: number) =&gt; [Application](./core.application.md)<!-- -->; getMaxListeners: () =&gt; number; listeners: (event: string \| symbol) =&gt; Function\[\]; rawListeners: (event: string \| symbol) =&gt; Function\[\]; emit: (event: string \| symbol, ...args: any\[\]) =&gt; boolean; listenerCount: (event: string \| symbol) =&gt; number; prependListener: (event: string \| symbol, listener: (...args: any\[\]) =&gt; void) =&gt; [Application](./core.application.md)<!-- -->; prependOnceListener: (event: string \| symbol, listener: (...args: any\[\]) =&gt; void) =&gt; [Application](./core.application.md)<!-- -->; eventNames: () =&gt; (string \| symbol)\[\]; }; } &amp; T

A new class that extends the super class with repository related methods

## Example


```ts
class MyApplication extends RepositoryMixin(Application) {}
```
Please note: the members in the mixin function are documented in a dummy class called <a href="#RepositoryMixinDoc">RepositoryMixinDoc</a>


