---
lang: en
title: 'API docs: authentication.useridentityservice.linkexternalprofile'
keywords: LoopBack 4.0, LoopBack 4, Node.js, TypeScript, OpenAPI
sidebar: lb4_sidebar
editurl: https://github.com/loopbackio/loopback-next/tree/master/packages/authentication
permalink: /doc/en/lb4/apidocs.authentication.useridentityservice.linkexternalprofile.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/authentication](./authentication.md) &gt; [UserIdentityService](./authentication.useridentityservice.md) &gt; [linkExternalProfile](./authentication.useridentityservice.linkexternalprofile.md)

## UserIdentityService.linkExternalProfile() method

link an external profile with an existing local user id.

<b>Signature:</b>

```typescript
linkExternalProfile(userId: string, userIdentity: I): Promise<U>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  userId | string |  |
|  userIdentity | I |  |

<b>Returns:</b>

Promise&lt;U&gt;

## Example

async linkExternalProfile(userId: string, ldapUser: LDAPUserIdentity) { return await this.userIdentityRepository.findOrCreate(<!-- -->{ provider: 'ldap', externalId: ldapUser.id, authScheme: 'active-directory', userId: userId, credentials: { distinguishedName: ldapUser.dn, roles: ldapUser.memberof, expirationTime: ldapUser.maxAge<!-- -->} }<!-- -->); } }


