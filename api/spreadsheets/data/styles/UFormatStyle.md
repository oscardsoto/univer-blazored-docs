---
layout: page
title: UFormatStyle
parent: Styles
grand_parent: Data
nav_order: 16
---

# {{ page.title }}

Cell value format config

```csharp
public struct UFormatStyle
```

## Remarks

This struct is used to define a formatting pattern for cell values, determining if they should be treated as numbers or dates based on the pattern's characters.

## Properties

|Property|Type|Description|
|---|---|---|
|pattern|string|Format Pattern Value|

## Methods

### IsForNumber

```csharp
public bool IsForNumber()
```

Return true if the pattern is numeric

##### Returns

bool: True if the pattern includes numeric placeholders like `#`, `0`, or `?`

---------

### IsForDate

```csharp
public bool IsForDate()
```

Return true if the pattern is for dates

##### Returns

bool: True if the pattern includes date/time markers like `M`, `D`, `A`, `H`, or `S`