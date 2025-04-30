---
layout: page
title: URankConfig
parent: Conditional Format
grand_parent: Data
nav_order: 16
---

# {{ page.title }}

Conditional format configuration for Rank type, from Univer

```csharp
public struct URankConfig
```

## Remarks

Defines the configuration for conditional formatting based on rank, such as top/bottom values or percentiles.

## Properties

|Property|Type|Description|
|---|---|---|
|isBottom|bool|True if the condition will begin at the bottom|
|isPercent|bool|True if the value is a percentage|
|value|double|Value to evaluate|

## Constructors

```csharp
public URankConfig()
```

Conditional format configuration for Rank type, from Univer

---------

```csharp
public URankConfig(bool isBottom, bool isPercent, double value)
```

Conditional format configuration for Rank type, from Univer

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|isBottom|bool|True if the condition will begin at the bottom|
|isPercent|bool|True if the value is a percentage|
|value|double|Value to evaluate|