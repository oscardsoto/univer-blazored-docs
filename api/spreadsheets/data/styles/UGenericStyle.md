---
layout: page
title: UGenericStyle
parent: Condition Format
grand_parent: Data
nav_order: 17
---

# {{ page.title }}

Style struct for deserialization, based on IStyleBase (See interface for doc)

```csharp
public struct UGenericStyle : IStyleBase
```

## Remarks

This struct is used to deserialize style data in a generic format compatible with the IStyleBase interface, allowing consistent styling across conditional formatting features.

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