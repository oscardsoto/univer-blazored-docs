---
layout: page
title: UFontProperties
parent: Styles
grand_parent: Data
nav_order: 12
---

# {{ page.title }}

Combines all Fonts characteristics to apply in range

```csharp
public struct UFontProperties
```

## Remarks

This struct groups all font-related style configurations such as color, size, alignment, and formatting options to be applied over a specific cell or range within a spreadsheet.

## Properties

|Property|Type|Description|
|---|---|---|
|Color|string?|Font Color|
|BackgroundColor|string?|Background Cell's color|
|Family|string?|Font family|
|Strikethrough|bool?|Font Line (line-through)|
|Underline|bool?|Font Line (line-through)|
|Size|double?|Font size|
|TextRotation|int?|Text Rotation (angle in degrees)|
|Italic|bool?|Font Style|
|Bold|bool?|Font Weight|
|HorizontalAlign|[FHorizontalAligment]({% link api/spreadsheets/data/styles/FHorizontalAligment.md %})?|Font Horizontal Align|
|VerticalAlign|[FVerticalAligment]({% link api/spreadsheets/data/styles/FVerticalAligment.md %})?|Font Vertical Align|
|NumberFormat|string?|Font format for number/Date|
|IsWrap|bool?|Font Wrap for the cells|
|WrapStrategy|[EWrapStrategy]({% link api/spreadsheets/data/styles/EWrapStrategy.md %})?|Font Wrap Strategy|

## Constructors

```csharp
public UFontProperties()
```

Combines all Fonts characteristics to apply in range