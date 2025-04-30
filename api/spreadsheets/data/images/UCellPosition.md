---
layout: page
title: UCellPosition
parent: Images
grand_parent: Data
nav_order: 3
---

# {{ page.title }}

ICellPosition, from Univer  
(See [Univer Docs](https://github.com/dream-num/univer/blob/dev/packages/sheets-drawing/src/services/sheet-drawing.service.ts#L64))

```csharp
public struct UCellPosition
```

## Remarks

Defines the position of an element (such as an image) inside a cell in terms of its row, column, and EMU offsets.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| column | int | Column number |
| columnOffset | double | Column offset, unit is EMUs |
| row | int | Row number |
| rowOffset | double | Row offset, unit is EMUs |
