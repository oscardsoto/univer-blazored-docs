---
layout: page
title: UTransform
parent: Images
grand_parent: Data
nav_order: 7
---

# {{ page.title }}

ITransformState, from Univer  
(See [Univer Docs](https://github.com/dream-num/univer/blob/dev/packages/core/src/types/interfaces/i-document-data.ts))

```csharp
public struct UTransform
```

## Remarks

Defines the visual transformation state of an image, including flipping, rotation, skewing, and pixel-based positioning. This struct is used to store the exact rendered shape of an image inside a spreadsheet.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| flipY | bool | True if the image should be flipped along the Y axis (horizontally). |
| flipX | bool | True if the image should be flipped along the X axis (vertically). |
| angle | int | The rotation angle of the image in degrees. A positive value rotates clockwise. |
| skewX | double | Specifies the horizontal skew angle for the image, in degrees. |
| skewY | double | Specifies the vertical skew angle for the image, in degrees. |
| left | double | Distance from the left edge of the containing cell to the left side of the image, in pixels. |
| top | double | Distance from the top edge of the containing cell to the top side of the image, in pixels. |
| width | double | Width of the image, in pixels. |
| height | double | Height of the image, in pixels. |
