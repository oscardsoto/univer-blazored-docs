---
layout: page
title: UConditionFormatStyle
parent: Conditional Format
grand_parent: Data
nav_order: 11
---

# UConditionFormatStyle

Conditional Format Style for the builder  
[See doc from Univer](https://reference.univer.ai/en-US/classes/FConditionalFormattingBuilder#setaverage)

```csharp
public struct UConditionFormatStyle
```

## Remarks

Represents a set of conditional formatting styles and rules that can be applied through a builder pattern. Each property is optional and corresponds to a particular conditional formatting configuration (e.g., average, color scale, data bar, font styles, etc). If a property is `null` or `false`, it is ignored.

## Properties

| Property        | Type                                                   | Description |
|-----------------|--------------------------------------------------------|-------------|
| Average         | [UAverageHighlightCell]({% link api/spreadsheets/data/conditional-format/UAverageHighlightCell.md %})? | Set average rule (null to ignore) |
| Background      | string                                                 | Sets the background color (null to ignore) |
| IsBold          | bool?                                                  | Set Bold (null to ignore) |
| ColorScale      | [UColorScale]({% link api/spreadsheets/data/conditional-format/UColorScale.md %})?  | Set colorScale rule (null to ignore) |
| DataBar         | [UDataBarConfig]({% link api/spreadsheets/data/conditional-format/UDataBarConfig.md %})? | Set dataBar rule (null to ignore) |
| DuplicateValues | bool                                                   | Set duplicateValues rule (false to ignore) |
| FontColor       | string                                                 | Sets the font color (null to ignore) |
| IconSet         | (bool isShowValue, [UIconSetConfig]({% link api/spreadsheets/data/conditional-format/UIconSetConfig.md %})[] config)? | Set iconSet rule (null to ignore) |
| Italic          | bool?                                                  | Set the text to italic (null to ignore) |
| Rank            | (bool isBottom, bool isPercent, double value)?         | Set rank rule (null to ignore) |
| Strikethrough   | bool?                                                  | Set the strikethrough (null to ignore) |
| Underline       | bool?                                                  | Set the underscore (null to ignore) |
| UniqueValues    | bool                                                   | Set uniqueValues rule (false to ignore) |