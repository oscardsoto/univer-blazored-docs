---
layout: page
title: UniverSpreadsheetConverterConfig
parent: Spreadsheet Converter API
nav_order: 3
---

# {{ page.title }}

Configuration object for the Converter Scoped.

```csharp
public class UniverSpreadsheetConverterConfig
```

## Remarks

Defines configuration settings for how the spreadsheet converter processes workbook data.

## Properties

|Property|Type|Description|
|---|---|---|
|MaxCellsReaded|int|Number of cells to process per task in the workbook. Default value is 1000.|