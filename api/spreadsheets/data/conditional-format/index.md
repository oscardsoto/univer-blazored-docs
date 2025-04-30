---
layout: page
title: Conditional Format
parent: Data
grand_parent: Spreadsheets
---
# Namespace
## UniverBlazored.Spreadsheets.Data.ConditionFormat

## Remarks

This namespace contains all data used in Univer to manage the conditional formats inside the UI, used to get all attributes and characteristics from the condition.

Most of the enums and classes enlisted here are similar (or equal) interfaces and classes from Univer's original API.

## Important notes
- An object with an "E" at the beginning indicates an Enumerator
- An object with an "U" at the beginning indicates a Class or a Struct

## Example

Normally, the conditional format is constructed through [Agent]({% link api/spreadsheets/services/UniverSpreadsheetAgent.md %}), and after getting all information, it can be used to get specific attributes:

```csharp
var conditions = await agent.GetAllConditionalFormats();
var colorScale = conditions[0].GetColorScaleConfigs();
...
var valueType = colorScale[i].value.GetValueType()
```