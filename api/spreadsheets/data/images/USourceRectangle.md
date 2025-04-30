---
layout: page
title: USourceRectangle
parent: Images
grand_parent: Data
nav_order: 6
---

# {{ page.title }}

ISrcRect, from Univer  
(See [Univer Docs](https://github.com/dream-num/univer/blob/dev/packages/core/src/shared/shape.ts#L37))

```csharp
public struct USourceRectangle
```

## Remarks

Defines the cropping margins for an image, used to trim the edges of an image source in a spreadsheet drawing context.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| left | int | Left crop |
| top | int | Top crop |
| bottom | int | Bottom crop |
| right | int | Right crop |