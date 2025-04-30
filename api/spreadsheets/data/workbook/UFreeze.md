---
layout: page
title: UFreeze
parent: Workbook
grand_parent: Data
nav_order: 1
---

# {{ page.title }}

IFreeze, from Univer. [See doc](https://univer.ai/typedoc/@univerjs/core/interfaces/IFreeze)

```csharp
public struct UFreeze
```

## Remarks

Represents the freeze state of a spreadsheet view, indicating how many rows and columns are frozen and where the scrollable area starts.

## Properties

|Property|Type|Description|
|---|---|---|
|startColumn|int|Scrollable start column (viewMain start column)|
|startRow|int|Scrollable start row (viewMain start row)|
|xSplit|int|Count of fixed (frozen) columns|
|ySplit|int|Count of fixed (frozen) rows|