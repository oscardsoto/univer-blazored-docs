---
layout: page
title: UTextRun
parent: Rich Text
grand_parent: Data
nav_order: 2
---

# {{ page.title }}

ITextRun, from Univer [See doc](https://github.com/dream-num/univer/blob/dev/packages/core/src/types/interfaces/i-document-data.ts#L333)

```csharp
public struct UTextRun
```

## Remarks

This struct represents a styled text range from the Univer document model. It defines the start and end positions of a style, the style identifier, and the corresponding text style configuration.

## Properties

|Property|Type|Description|
|---|---|---|
|st|int|Start for styling|
|ed|int|End styling|
|sId|string|Style Id|
|ts|[UTextStyle]({% link api/spreadsheets/data/rich-text/UTextStyle.md %})|Text Style|