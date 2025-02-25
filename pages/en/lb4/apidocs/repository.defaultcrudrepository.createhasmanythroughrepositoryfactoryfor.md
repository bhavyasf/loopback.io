---
lang: en
title: 'API docs: repository.defaultcrudrepository.createhasmanythroughrepositoryfactoryfor'
keywords: LoopBack 4.0, LoopBack 4, Node.js, TypeScript, OpenAPI
sidebar: lb4_sidebar
editurl: https://github.com/loopbackio/loopback-next/tree/master/packages/repository
permalink: /doc/en/lb4/apidocs.repository.defaultcrudrepository.createhasmanythroughrepositoryfactoryfor.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/repository](./repository.md) &gt; [DefaultCrudRepository](./repository.defaultcrudrepository.md) &gt; [createHasManyThroughRepositoryFactoryFor](./repository.defaultcrudrepository.createhasmanythroughrepositoryfactoryfor.md)

## DefaultCrudRepository.createHasManyThroughRepositoryFactoryFor() method

Function to create a constrained hasManyThrough relation repository factory

<b>Signature:</b>

```typescript
protected createHasManyThroughRepositoryFactoryFor<Target extends Entity, TargetID, Through extends Entity, ThroughID, ForeignKeyType>(relationName: string, targetRepositoryGetter: Getter<EntityCrudRepository<Target, TargetID>> | {
        [repoType: string]: Getter<EntityCrudRepository<Target, TargetID>>;
    }, throughRepositoryGetter: Getter<EntityCrudRepository<Through, ThroughID>>): HasManyThroughRepositoryFactory<Target, TargetID, Through, ForeignKeyType>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  relationName | string | Name of the relation defined on the source model |
|  targetRepositoryGetter | [Getter](./context.getter.md)<!-- -->&lt;[EntityCrudRepository](./repository.entitycrudrepository.md)<!-- -->&lt;Target, TargetID&gt;&gt; \| { \[repoType: string\]: [Getter](./context.getter.md)<!-- -->&lt;[EntityCrudRepository](./repository.entitycrudrepository.md)<!-- -->&lt;Target, TargetID&gt;&gt;; } |  |
|  throughRepositoryGetter | [Getter](./context.getter.md)<!-- -->&lt;[EntityCrudRepository](./repository.entitycrudrepository.md)<!-- -->&lt;Through, ThroughID&gt;&gt; |  |

<b>Returns:</b>

[HasManyThroughRepositoryFactory](./repository.hasmanythroughrepositoryfactory.md)<!-- -->&lt;Target, TargetID, Through, ForeignKeyType&gt;

## Example


```ts
class CustomerRepository extends DefaultCrudRepository<
  Customer,
  typeof Customer.prototype.id,
  CustomerRelations
> {
  public readonly cartItems: HasManyRepositoryFactory<CartItem, typeof Customer.prototype.id>;

  constructor(
    protected db: juggler.DataSource,
    cartItemRepository: EntityCrudRepository<CartItem, typeof, CartItem.prototype.id>,
    throughRepository: EntityCrudRepository<Through, typeof Through.prototype.id>,
  ) {
    super(Customer, db);
    this.cartItems = this.createHasManyThroughRepositoryFactoryFor(
      'cartItems',
      cartItemRepository,
    );
  }
}
```


