---
layout: page
title: UStyleData
parent: Styles
grand_parent: Data
nav_order: 19
---

# {{ page.title }}

IStyleData, from Univer  
See doc: [Univer TypeDoc - IStyleData](https://univer.ai/typedoc/@univerjs/core/interfaces/IStyleData)

```csharp
public class UStyleData : IStyleBase
```

## Remarks

Represents the full styling information for a cell or element, with support for nullables to allow optional property assignment.

> **Note:** This class must be used instead of a struct to support nullable properties.

## Properties

| Property | Type | Default | Description |
|----------|------|---------|-------------|
| bbl      | [UTextDecoration]({% link api/spreadsheets/data/styles/UTextDecoration.md %})? | null | Bottom border line |
| bd       | [UBorderData]({% link api/spreadsheets/data/styles/UBorderData.md %})?     | null | Border data |
| bg       | [UColorStyle]({% link api/spreadsheets/data/styles/UColorStyle.md %})?     | null | Background color |
| bl       | int              | 0    | Bold (0: false, 1: true) |
| cl       | [UColorStyle]({% link api/spreadsheets/data/styles/UColorStyle.md %})?     | null | Font color (foreground) |
| ff       | string           | Arial | Font family |
| fs       | int              | 10   | Font size |
| ht       | [EHorizontalAlign]({% link api/spreadsheets/data/styles/EHorizontalAlign.md %}) | UNSPECIFIED | Horizontal alignment |
| it       | int              | 0    | Italic (0: false, 1: true) |
| n        | [UFormatStyle]({% link api/spreadsheets/data/styles/UFormatStyle.md %})?    | null | Number format pattern |
| ol       | [UTextDecoration]({% link api/spreadsheets/data/styles/UTextDecoration.md %})  | new() | Overline decoration |
| pd       | [UPaddingData]({% link api/spreadsheets/data/styles/UPaddingData.md %})     | new() | Padding values |
| st       | [UTextDecoration]({% link api/spreadsheets/data/styles/UTextDecoration.md %})  | new() | Strikethrough decoration |
| tb       | [EWrapStrategy]({% link api/spreadsheets/data/styles/EWrapStrategy.md %})    | UNSPECIFIED | Wrap strategy |
| td       | [ETextDirection]({% link api/spreadsheets/data/styles/ETextDirection.md %})   | UNSPECIFIED | Text direction |
| tr       | [UTextRotation]({% link api/spreadsheets/data/styles/UTextRotation.md %})?   | null | Text rotation |
| ul       | [UTextDecoration]({% link api/spreadsheets/data/styles/UTextDecoration.md %})  | new() | Underline decoration |
| vt       | [EVerticalAlign]({% link api/spreadsheets/data/styles/EVerticalAlign.md %})?  | null | Vertical alignment |
| va       | object?          | null | Subscript (only for Chinese, obsolete) |

## Methods

### IsDefault(UStyleData style)

Returns true if the given style object only contains default values (i.e., no meaningful formatting set).

```csharp
public static bool IsDefault(UStyleData style)
```

#### Returns

true if all values are default; otherwise, false.