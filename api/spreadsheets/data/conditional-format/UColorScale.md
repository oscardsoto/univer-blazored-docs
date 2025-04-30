---
layout: page
title: UColorScale
parent: Conditional Format
grand_parent: Data
nav_order: 8
---

# {{ page.title }}

IColorScale, from Univer [See doc:](https://github.com/dream-num/univer/blob/dev/packages/sheets-conditional-formatting/src/models/type.ts#L91)

```csharp
public struct UColorScale
```

## Remarks

Defines a color scale rule for conditional formatting, mapping data values to color ranges based on provided configuration objects.

## Properties

|Property|Type|Description|
|---|---|---|
|type|string|[ECFRuleType]({% link api/spreadsheets/data/conditional-format/ECFRuleType.md %}) value|
|config|[UColorScaleConfig]({% link api/spreadsheets/data/conditional-format/UColorScaleConfig.md %})[]|Configuration objects for each situation|

## Constructors

```csharp
public UColorScale()
```

IColorScale, from Univer [See doc:](https://github.com/dream-num/univer/blob/dev/packages/sheets-conditional-formatting/src/models/type.ts#L91)