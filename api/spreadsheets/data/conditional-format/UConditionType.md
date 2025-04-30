---
layout: page
title: UConditionType
parent: Conditional Format
grand_parent: Data
nav_order: 12
---

# UConditionType

Sets where the conditional format needs to trigger

```csharp
public struct UConditionType
```

## Remarks

Defines the set of logical conditions under which a conditional formatting rule should be applied to a cell. Each property corresponds to a specific condition type (text, number, date, formula, etc). If a property is `null` or `false`, it is ignored.

## Properties

| Property                    | Type                                 | Description |
|-----------------------------|--------------------------------------|-------------|
| WhenCellEmpty               | bool                                 | Sets the conditional formatting rule to fire when the cell is empty. (False to ignore) |
| WhenCellNotEmpty            | bool                                 | Sets the conditional formatting rule to fire when the cell is not empty. (False to ignore) |
| WhenDate                    | [ECFOperators]({% link api/spreadsheets/data/conditional-format/ECFOperators.md %})?                        | Highlight when the date is in a time period. (null to ignore). Only valid for Time Period operators. Throws if invalid. |
| WhenFormulaSatisfied        | string                               | Sets a conditional formatting rule to fire when a given formula evaluates to true. (null to ignore) |
| WhenNumberInBetween         | (double start, double ends)?         | Fires when a number is between two specified values or equal to one of them. (null to ignore) |
| WhenNumberEqualTo           | double?                              | Fires when the number equals the given value. (null to ignore) |
| WhenNumberGreaterThan       | double?                              | Fires when the number is greater than the given value. (null to ignore) |
| WhenNumberGreaterThanOrEqual | double?                            | Fires when a number is greater than or equal to a given value. (null to ignore) |
| WhenNumberLessThan          | double?                              | Fires when the number is less than the given value. (null to ignore) |
| WhenNumberLessThanOrEqual   | double?                              | Fires when the number is less than or equal to the given value. (null to ignore) |
| WhenNumberNotBetween        | (double start, double ends)?         | Fires when a number is not between two specified values and is not equal to them. (null to ignore) |
| WhenNumberNotEqual          | double?                              | Fires when a number does not equal a given value. (null to ignore) |
| WhenTextContains            | string                               | Fires when the input contains the given value. (null to ignore) |
| WhenTextDoesNotContain      | string                               | Fires when the input does not contain the given value. (null to ignore) |
| WhenTextEndsWith            | string                               | Fires when input ends with a specified value. (null to ignore) |
| WhenTextEqualTo             | string                               | Fires when the input equals the given value. (null to ignore) |
| WhenTextStartsWith          | string                               | Fires when the input value begins with the given value. (null to ignore) |
| IsIconSet                   | bool                                 | Sets the conditional formatting rule for Icon Set (false to ignore) |
| IsColorScale                | bool                                 | Sets the conditional formatting rule for Color Scale (false to ignore) |
| IsDataBar                   | bool                                 | Sets the conditional formatting rule for Data Bar (false to ignore) |