---
layout: page  
title: UniverUser
parent: Data  
grand_parent: Generic  
nav_order: 4
---

# {{ page.title }}

Univer User's data from the UserManager

```csharp
public struct UniverUser
```

## Remarks

This struct represents a Univer platform user, including identification, display name, avatar, and user type information.

## Properties

|Property|Type|Description|
|---|---|---|
|id|string|User id|
|name|string|User's name|
|avatar|string|Image of the user (in Data Uri format)|
|Type|[UniverUserType]({% link api/generic/data/UniverUserType.md %})|User's type|

## Methods

### GetUserType

```csharp
public UniverUserType GetUserType()
```

Get the user's type

##### Returns

[UniverUserType]({% link api/generic/data/UniverUserType.md %}): Resolved user type from ID content

---------

### SetUserType

```csharp
public void SetUserType(UniverUserType type)
```

Set the user type

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|type|[UniverUserType]({% link api/generic/data/UniverUserType.md %})|New type for the User ID|

---------