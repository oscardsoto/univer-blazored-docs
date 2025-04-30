---
layout: page  
title: UniverResponse
parent: Data  
grand_parent: Generic  
nav_order: 3
---

# {{ page.title }}

Response for the result of the queue execution

```csharp
public class UniverResponse<TValue>
```

## Remarks

This generic class wraps the result of a queue execution, providing a strongly-typed response value.

## Properties

|Property|Type|Description|
|---|---|---|
|res|TValue|Result for that process, in the desired value|  