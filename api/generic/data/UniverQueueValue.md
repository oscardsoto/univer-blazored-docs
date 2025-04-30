---
layout: page  
title: UniverQueueValue
parent: Data  
grand_parent: Generic  
nav_order: 2
---

# {{ page.title }}

Queue info to resolve in Univer's core

```csharp
public struct UniverQueueValue
```

## Remarks

This struct represents a queue entry containing a method name and its arguments, intended to be processed by Univer's core logic.

## Properties

|Property|Type|Description|
|---|---|---|
|methodName|string|Method name|
|args|object[]|Arguments for that method (make sure that each argument is serializable)|

## Constructors

```csharp
public UniverQueueValue()
```

Queue info to resolve in Univer's core

---------

```csharp
public UniverQueueValue(string methodName, params object[] args)
```

Queue info to resolve in Univer's core

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|methodName|string|Method name|
|args|object[]|Arguments for that method (make sure that each argument is serializable)|

---------