---
layout: page
title: UTextStyle
parent: Rich Text
grand_parent: Data
nav_order: 3
---

# {{ page.title }}

ITextStyle, from Univer [See doc](https://github.com/dream-num/univer/blob/dev/packages/core/src/types/interfaces/i-document-data.ts#L704)

```csharp
public struct UTextStyle : IStyleBase
```

## Remarks

This struct defines the styling attributes for rich text segments, including font settings, decorations, colors, spacing, and other advanced typographic options used in Univer documents.

## Properties

|Property|Type|Description|
|---|---|---|
|sc|int?|Spacing|
|pos|int?|Position|
|sa|int?|Scale|
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