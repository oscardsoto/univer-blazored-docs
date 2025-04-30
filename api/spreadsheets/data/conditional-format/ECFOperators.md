---
layout: page
title: ECFOperators
parent: Conditional Format
grand_parent: Data
nav_order: 1
---

# {{ page.title }}

Group of all operator types in Univer

```csharp
[Flags]
public enum ECFOperators
```

## Fields

|Value|Name|Descrpition|
|---|---|---|
|0|beginsWith|Matches if source value starts with specified text.|
|1|endsWith|Matches if source value ends with specified text.|
|2|containsText|Matches if source value includes the specified text anywhere within it.|
|3|notContainsText|Does not match if source value includes the specified text.|
|4|equal|Matches when both values are exactly the same.|
|5|notEqual|Matches if values are not exactly the same.|
|6|containsBlanks|Matches when source value includes at least one white space character.|
|7|notContainsBlanks|Does not match if the source value includes no white space characters.|
|8|containsErrors|Matches when error flag is set for any character in the text string.|
|9|notContainsErrors|Does not match if no characters have an error flag set.|
|10|today|Matches the current date exactly.|
|11|yesterday|Matches one day prior to the current date.|
|12|tomorrow|Matches one day after the current date.|
|13|last7Days|Matches any date within the past seven days.|
|14|lastMonth|Matches any day within the previous month.|
|15|thisMonth|Matches any day in the current month.|
|16|nextMonth|Matches any day within the following month.|
|17|lastWeek|Matches any week within the previous year.|
|18|thisWeek|Matches any day in the current week.|
|19|nextWeek|Matches any day within the following week.|
|20|greaterThan|Matches when source value is larger than specified number.|
|21|greaterThanOrEqual|Matches when source value is larger or equal to the specified number.|
|22|lessThan|Matches when source value is smaller than specified number.|
|23|lessThanOrEqual|Matches when source value is smaller or equal to the specified number.|
|24|notBetween|Does not match if source value is within the range of two specified numbers.|
|25|between|Matches if source value falls in a defined range of minimum and maximum values.|

## Remarks

