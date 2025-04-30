---
layout: page
title: IUniverSpreadsheetConverter
nav_order: 1
parent: Spreadsheet Converter API
---

# {{ page.title }}

Interface for managing spreadsheet data.  
Provides methods to set/get data into/from an XLWorkbook using agent and userManager details, and optionally just populate data.

```csharp
public interface IUniverSpreadsheetConverter
```

## Remarks

This interface defines a contract for interacting with spreadsheet data using Univer's spreadsheet model, allowing population or extraction of data from workbooks and worksheets with contextual support from agent and user manager instances.

## Methods

### SetInformationAsync

```csharp
Task<XLWorkbook> SetInformationAsync(UniverSpreadsheetAgent agent, UniverUserManager userManager, SpreadsheetOptions options)
```

Setup spreadsheet data based on provided agent and userManager.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|agent|[UniverSpreadsheetAgent]({% link api/spreadsheets/services/UniverSpreadsheetAgent.md %})|Agent for setting up the workbook.|
|userManager|[UniverUserManager]({% link api/generic/services/UniverUserManager.md %})|User service for setting up the workbook.|
|options|[SpreadsheetOptions]({% link spreadsheet-converter/SpreadsheetOptions.md %})|Flags to select which data will be set.|

##### Returns

`Task<XLWorkbook>`: A task that returns the configured workbook.

---------

### GetInformationInAgentAsync

```csharp
Task GetInformationInAgentAsync(XLWorkbook excelWorkbook, UniverSpreadsheetAgent agent, UniverUserManager userManager, SpreadsheetOptions options)
```

Get data into a workbook using provided agent and worksheet.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|excelWorkbook|[XLWorkbook](https://docs.closedxml.io/en/latest/api/index.html#class-ClosedXML.Excel.XLWorkbook)|Workbook containing source data for getting into an agent.|
|agent|[UniverSpreadsheetAgent]({% link api/spreadsheets/services/UniverSpreadsheetAgent.md %})|Agent for storing fetched data.|
|userManager|[UniverUserManager]({% link api/generic/services/UniverUserManager.md %})|User service for setting up the workbook.|
|options|[SpreadsheetOptions]({% link spreadsheet-converter/SpreadsheetOptions.md %})|Flags to select which data will be set.|

##### Returns

Task: Represents the asynchronous operation.

---------

### GetInformationInAgentAsync

```csharp
Task GetInformationInAgentAsync(IXLWorksheet worksheet, UniverSpreadsheetAgent agent, UniverUserManager userManager, SpreadsheetOptions options)
```

Gets information into an agent from a worksheet (IXLWorksheet).

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|worksheet|[IXLWorksheet](https://docs.closedxml.io/en/latest/api/worksheet.html#interface-ClosedXML.Excel.IXLWorksheet)|Worksheet containing source data for getting into an agent.|
|agent|[UniverSpreadsheetAgent]({% link api/spreadsheets/services/UniverSpreadsheetAgent.md %})|Agent for storing fetched data.|
|userManager|[UniverUserManager]({% link api/generic/services/UniverUserManager.md %})|User service for setting up the workbook.|
|options|[SpreadsheetOptions]({% link spreadsheet-converter/SpreadsheetOptions.md %})|Flags to select which data will be set.|

##### Returns

Task: Represents the asynchronous operation.

---------

### SetInformationInSheetAsync

```csharp
Task SetInformationInSheetAsync(XLWorkbook workbook, USheetInfo unvrSheet, UniverSpreadsheetAgent agent, UniverUserManager userManager, SpreadsheetOptions options)
```

Sets spreadsheet data based on provided agent and userManager.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|workbook|[XLWorkbook](https://docs.closedxml.io/en/latest/api/index.html#class-ClosedXML.Excel.XLWorkbook)|Workbook to put the sheet data.|
|unvrSheet|[USheetInfo](% link api/spreadsheets/data/workbook/USheetInfo.md %)|Data of the sheet (Univer) that will be read.|
|agent|[UniverSpreadsheetAgent]({% link api/spreadsheets/services/UniverSpreadsheetAgent.md %})|Univer's agent.|
|userManager|[UniverUserManager]({% link api/generic/services/UniverUserManager.md %})|Univer's user manager.|
|options|[SpreadsheetOptions]({% link spreadsheet-converter/SpreadsheetOptions.md %})|Flags to select which data will be set.|

##### Returns

Task: Represents the asynchronous operation.