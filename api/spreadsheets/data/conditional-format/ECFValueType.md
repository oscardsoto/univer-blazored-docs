---
layout: page
title: ECFValueType
parent: Conditional Format
grand_parent: Data
nav_order: 5
---

# {{ page.title }}

CFValueType, form Univer [See doc:](https://github.com/dream-num/univer/blob/dev/packages/sheets-conditional-formatting/src/base/const.ts#L73)

```csharp
public enum ECFValueType
```

## Fields

|Name|Value|Descrpition|
|---|---|---|
|num|0|Represents a numerical value (i.e., 1,234).|
|min|1|Represents the minimum possible value for the type of data being evaluated.|
|max|2|Represents the maximum possible value for the type of data being evaluated.|
|percent|3|Represents a percentage (i.e., 25%, 75%).|
|percentile|4|Represents the value at a particular percentile within the dataset. For example, 90th percentile represents the highest 10% of data values.|
|formula|5|Represents a formula result (i.e., SUM(A:B), AVG(C:D)).|

## Remarks
This enum defines the types of values used in conditional formatting evaluations, supporting both static values and dynamic formula-based logic.