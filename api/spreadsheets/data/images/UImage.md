---
layout: page
title: UImage
parent: Images
grand_parent: Data
nav_order: 4
---

# {{ page.title }}

IFOverGridImage, from Univer  
(see [Univer Docs](https://github.com/dream-num/univer/blob/dev/packages/sheets-drawing-ui/src/facade/f-over-grid-image.ts#L27))

```csharp
public struct UImage
```

## Remarks

Represents an image object placed over the grid in a spreadsheet, including its source, positioning, and transformation details.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| unitId | string | Workbook Id |
| subUnitId | string | Worksheet Id |
| drawingId | string | Image id on Univer |
| drawingType | [EDrawingType]({% link api/spreadsheets/data/images/EDrawingType.md %}) | Image type |
| imageSourceType | string | Type of source for the image |
| source | string | Data Uri for the image (originally a string) |
| sheetTransform | [USheetTransform]({% link api/spreadsheets/data/images/USheetTransform.md %}) | Position in Sheet |
| transform | [UTransform]({% link api/spreadsheets/data/images/UTransform.md %}) | Transform state |
| srcRect | [USourceRectangle]({% link api/spreadsheets/data/images/USourceRectangle.md %})? | Source Rectangle (from cropping the image) |

## Constructors

```csharp
public UImage()
```

Default constructor.

---

## Methods

```csharp
public string GetBase64()
```

Returns the base64 data from the Data URI source.

### Returns

`string` — The base64 part of the Data URI, or the original `source` string if null or empty.

---

```csharp
public string GetImageType()
```

Returns the image MIME type from the Data URI source.

### Returns

`string` — The MIME type (e.g., `image/png`) extracted from the Data URI, or the original `source` if null or empty.

---