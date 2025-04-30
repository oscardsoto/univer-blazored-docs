---
layout: page
title: USheetInfo
parent: Workbook
grand_parent: Data
nav_order: 3
---

# {{ page.title }}

Info for the sheet.

```csharp
public struct USheetInfo
```

## Remarks

Contains metadata related to an individual sheet, including its identifier, name, visual settings, and used range.

## Properties

| Property    | Type     | Description                      |
|-------------|----------|----------------------------------|
| id          | string   | Univer's Id for the sheet        |
| name        | string   | Sheet's name                     |
| maxUsed     | [URange]({% link api/spreadsheets/data/workbook/URange.md %})   | Range used in the sheet |
| tabColor    | string   | Tab color of the sheet (if any)  |