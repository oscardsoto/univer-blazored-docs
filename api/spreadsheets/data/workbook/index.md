---
layout: page
title: Workbook
parent: Data
grand_parent: Spreadsheets
---
# Namespace
## UniverBlazored.{{ page.grand_parent }}.{{page.parent}}.{{page.title}}

## Remarks

This namespace contains all data used in Univer to manage data from the workbook and worksheets from the UI.

Most of the enums and classes enlisted here are similar (or equal) interfaces and classes from Univer's original API.

## Important notes
- An object with an "E" or "F" at the beginning indicates an Enumerator
- An object with an "U" at the beginning indicates a Class or a Struct

## Example

After getting the sheets' data from the [Agent]({% link api/spreadsheets/services/UniverSpreadsheetAgent.md %}):

```csharp
var sheetInf = await agent.GetSheetsInfo();
foreach (var sheet in sheetInf)
{
    Console.WriteLine($"{sheet.name}");
}
```