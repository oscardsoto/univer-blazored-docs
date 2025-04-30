---
layout: page
title: UIconSetCond
parent: Conditional Format
grand_parent: Data
nav_order: 14
---

# {{ page.title }}

"config" object used in the FacadeAPI to construct an IconSet Conditional Format

```csharp
public struct UIconSetCond
```

## Remarks

This struct represents the configuration for an IconSet Conditional Format, used within the FacadeAPI to define icon display and behavior for conditional formatting rules in spreadsheets.

## Properties

|Property|Type|Description|
|---|---|---|
|isShowValue|bool|True to show the value in the cell|
|iconConfigs|[UIconSetConfig]({% link api/spreadsheets/data/conditional-format/UIconSetConfig.md %})[]|Configuration objects for each icon|

## Constructors

```csharp
public UIconSetCond()
```

"config" object used in the FacadeAPI to construct an IconSet Conditional Format

---------

```csharp
public UIconSetCond(bool isShowValue, UIconSetConfig[] iconConfigs)
```

"config" object used in the FacadeAPI to construct an IconSet Conditional Format

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|isShowValue|bool|True to show the value in the cell|
|iconConfigs|[UIconSetConfig]({% link api/spreadsheets/data/conditional-format/UIconSetConfig.md %})[]|Configuration objects for each icon|

---------