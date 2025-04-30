---
layout: page
title: UniverSpreadsheetListenerData
parent: Data
grand_parent: Spreadsheets
nav_order: 1
---

# {{ page.title }}

Data where the listener gets the information.

```csharp
public struct UniverSpreadsheetListenerData
```

## Remarks

Provides context for events or interactions within a spreadsheet, such as the selected cell and the associated workbook and worksheet identifiers.

## Properties

| Property    | Type     | Description                             |
|-------------|----------|-----------------------------------------|
| row         | int      | Selected Row                            |
| col         | int      | Selected Column                         |
| unitId      | string   | Workbook where the listener is stored   |
| subUnitId   | string   | Worksheet where the listener is located |