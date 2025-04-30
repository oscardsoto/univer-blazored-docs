---
layout: page
title: SpreadsheetOptions
parent: Spreadsheet Converter API
nav_order: 2
---

# {{ page.title }}

Option class for getting/setting the information from Univer's Agent.

```csharp
public class SpreadsheetOptions
```

## Remarks

This class encapsulates the different toggles that control which aspects of a spreadsheet (such as data, styles, merges, filters, etc.) should be processed during the import/export operations.

## Properties

|Property|Type|Description|
|---|---|---|
|RecData|bool|True to get/set spreadsheet data.|
|RecStyles|bool|True to get/set spreadsheet styles.|
|RecMerges|bool|True to get/set spreadsheet merges.|
|RecFilters|bool|True to get/set spreadsheet filters.|
|RecFreeze|bool|True to get/set spreadsheet freeze columns and rows.|
|RecComments|bool|True to get/set spreadsheet comments.|
|RecColumnsAndRows|bool|True to get/set spreadsheet columns and rows data.|
|RecImages|bool|True to get/set spreadsheet images.|
|RecConditionalFormats|bool|True to get/set spreadsheet conditional formats.|
|RecAccesibility|bool|True to get/set spreadsheet accessibility.|

## Constructors

### SpreadsheetOptions()

```csharp
public SpreadsheetOptions()
```

Default constructor. Initializes an empty instance of `SpreadsheetOptions` with all options unset.

---

### SpreadsheetOptions(bool RecAll)

```csharp
public SpreadsheetOptions(bool RecAll)
```

Initializes all options based on the provided boolean value.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|RecAll|bool|True to enable all options; False to disable all options.|