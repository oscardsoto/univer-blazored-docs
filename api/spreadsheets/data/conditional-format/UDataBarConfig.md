---
layout: page
title: UDataBarConfig
parent: Conditional Format
grand_parent: Data
nav_order: 13
---

# UDataBarConfig

DataBar configuration Object for the conditional format

```csharp
public struct UDataBarConfig
```

## Remarks

Represents the configuration for a conditional formatting Data Bar. This struct defines visual and value settings for displaying a horizontal bar within cells, based on the cell's value in relation to a defined range.

## Properties

| Property        | Type           | Description |
|----------------|----------------|-------------|
| isGradient     | bool           | True for a gradient data bar |
| isShowValue    | bool           | True to show the numerical value alongside the data bar |
| min            | [UValueConfig]({% link api/spreadsheets/data/conditional-format/UValueConfig.md %})   | Minimum value configuration for the data bar |
| max            | [UValueConfig]({% link api/spreadsheets/data/conditional-format/UValueConfig.md %})   | Maximum value configuration for the data bar |
| nativeColor    | string         | Color for negative values (Hexadecimal format) |
| positiveColor  | string         | Color for positive values (Hexadecimal format) |