---
layout: page
title: UColorScaleConfig
parent: Conditional Format
grand_parent: Data
nav_order: 9
---

# {{ page.title }}

Color Scale configuration Object for the conditional format

```csharp
public struct UColorScaleConfig
```

## Remarks

Represents an individual configuration entry in a color scale rule, defining a color, index, and value to map in the formatting scale.

## Properties

|Property|Type|Description|
|---|---|---|
|index|int|Color index|
|color|string|Color (in hexadecimal)|
|value|[UValueConfig]({% link api/spreadsheets/data/conditional-format/UValueConfig.md %})|Value for the Color scale to apply|