---
layout: page
title: USheetTransform
parent: Images
grand_parent: Data
nav_order: 5
---

# {{ page.title }}

ISheetDrawingPosition, from Univer  
(See [Univer Docs](https://github.com/dream-num/univer/blob/dev/packages/sheets-drawing/src/services/sheet-drawing.service.ts))

```csharp
public struct USheetTransform
```

## Remarks

Represents the full transformation of a drawing element (like an image) within the spreadsheet, including its position, rotation, flipping, and skewing.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| flipY | bool | True if the image should be flipped along the Y axis (horizontally). |
| flipX | bool | True if the image should be flipped along the X axis (vertically). |
| angle | int | Rotation angle |
| skewX | double | Specifies the horizontal skew angle for the image, in degrees. |
| skewY | double | Specifies the vertical skew angle for the image, in degrees. |
| from | [UCellPosition]({% link api/spreadsheets/data/images/UCellPosition.md %}) | Cell begin position |
| to | [UCellPosition]({% link api/spreadsheets/data/images/UCellPosition.md %}) | Cell end position |
