---
layout: page
title: IStyleBase
parent: Styles
grand_parent: Data
nav_order: 8
---

# {{ page.title }}

IStyleBase, from Univer [See doc](https://github.com/dream-num/univer/blob/dev/packages/core/src/types/interfaces/i-style-data.ts#L134)

```csharp
public interface IStyleBase
```

## Remarks

Defines a base interface for text styling used across Univer documents. It encapsulates common typographic features such as font, size, weight, decorations, colors, and formatting options.

## Properties

|Property|Type|Description|
|---|---|---|
|ff|string|fontFamily|
|fs|int|fontSize (pt)|
|it|int|italic — 0: false, 1: true|
|bl|int|bold — 0: false, 1: true|
|ul|[UTextDecoration]({% link api/spreadsheets/data/styles/UTextDecoration.md %})|underline|
|bbl|[UTextDecoration]({% link api/spreadsheets/data/styles/UTextDecoration.md %})?|bottomBorderLine|
|st|[UTextDecoration]({% link api/spreadsheets/data/styles/UTextDecoration.md %})|strikethrough|
|ol|[UTextDecoration]({% link api/spreadsheets/data/styles/UTextDecoration.md %})|overline|
|bg|[UColorStyle]({% link api/spreadsheets/data/styles/UColorStyle.md %})?|background|
|bd|[UBorderData]({% link api/spreadsheets/data/styles/UBorderData.md %})?|border|
|cl|[UColorStyle]({% link api/spreadsheets/data/styles/UColorStyle.md %})?|foreground|
|va|object?|Subscript/Superscript Text|
|n|[UFormatStyle]({% link api/spreadsheets/data/styles/UFormatStyle.md %})?|Number format pattern|