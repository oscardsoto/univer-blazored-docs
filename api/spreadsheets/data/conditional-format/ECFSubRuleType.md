---
layout: page
title: ECFSubRuleType
parent: Conditional Format
grand_parent: Data
nav_order: 4
---

# {{ page.title }}

CFSubRuleType, from Univer [See doc:](https://github.com/dream-num/univer/blob/dev/packages/sheets-conditional-formatting/src/base/const.ts#L55)

```csharp
public enum ECFSubRuleType
```

## Fields

|Name|Value|Descrpition|
|---|---|---|
|uniqueValues|0|Matches cells with unique values in the column or row.|
|duplicateValues|1|Matches cells with duplicate values in the column or row.|
|rank|2|Matches cells where the value is ranked based on other rules applied.|
|text|3|Matches cells where the text content matches a specified pattern or value.|
|timePeriod|4|Matches cells based on time period (e.g., today, yesterday, tomorrow).|
|number|5|Matches cells where the value is a number and meets specific conditions (greater than, less than, etc.).|
|average|6|Matches cells with an average calculation that matches specified conditions.|
|formula|7|Matches cells where the value is a result of a formula and meets specific conditions (e.g., cell values are used in calculations).|

## Remarks
This enum specifies sub-rule types used in conditional formatting logic within Univer, providing more granular rule categories based on data types and logic.