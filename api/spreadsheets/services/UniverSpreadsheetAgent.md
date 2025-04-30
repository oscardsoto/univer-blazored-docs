---
layout: page
title: UniverSpreadsheetAgent
parent: Services
grand_parent: Spreadsheets
nav_order: 2
---

# {{ page.title }}

Univer's agent. Enables operations inside Blazor

```csharp
public class UniverSpreadsheetAgent
```

## Remarks

This class is responsible for handling all operations within the Univer Excel sheet component. Each method sends a list of actions—along with their respective parameters—that the JavaScript layer must perform, and queues them in the SpreadsheetJsInterop for later processing. The result corresponds to the function being executed.

The agent is designed to execute any possible action within the Univer component, ranging from inserting a value into a cell to adding or removing an image from the current sheet.

## Constructor

```csharp
public UniverSpreadsheetAgent(IUniverJsInterop univerJS)
```

| Property | Type | Description |
|---------|------|-------------|
| univerJS | [IUniverJsInterop]({% link api/generic/IUniverJsInterop.md %}) | Univer's interop to get acces to Univer |

## Methods

### SetActiveSheet

```csharp
Task SetActiveSheet(string idSheet)
```

Sets the active sheet to the component.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|idSheet|string|Id of the sheet to put the changes.|

---

### SetActiveRange

```csharp
Task SetActiveRange(URange range)
```

Sets the range to work in the active sheet on the component.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|range|[URange]({% link api/spreadsheets/data/workbook/URange.md %})|Range object representing the active range.|

---

### GetSheetsInfo

```csharp
Task<USheetInfo[]> GetSheetsInfo()
```

Return all sheets information.

##### Returns

_[USheetInfo]({% link api/spreadsheets/data/workbook/USheetInfo.md %})[]_ — List of all sheets information

---

### AddNewSheet

```csharp
Task<USheetInfo> AddNewSheet(string sheetName, int rows, int cols, string hexColorTab = null)
```

Adds a new Worksheet in the active workbook.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|sheetName|string|Name of the new worksheet|
|rows|int|Amount of rows that the worksheet will have|
|cols|int|Amount of columns that the worksheet will have|
|hexColorTab|string|Color of its tab (in hexadecimal)|

##### Returns

_[USheetInfo]({% link api/spreadsheets/data/workbook/USheetInfo.md %})_ — Info object of the created worksheet

---

### DeleteSheet

```csharp
Task DeleteSheet(string idSheet = null)
```

Removes the specified sheet.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|idSheet|string|Id for the sheet to delete. If null or empty, deletes the active sheet|

---

### SetValue

```csharp
Task SetValue(object value)
```

Set a value on a specific Row/Col.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|value|object|The value to put on the cell|

---

### GetValue

```csharp
Task<TValue> GetValue<TValue>()
```

Gets the value in the specific Row/col. If not, return null.

##### Returns

_TValue_ — The value from the cell

---

### SetValue

```csharp
Task SetValue(params object[][] values)
```

Set values on a range.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|values|object[][]|Values of each row for the range. The size of each array must be the same number as the number of columns used|

---

### GetValues

```csharp
Task<object[][]> GetValues()
```

Gets all values in the range. If a cell in the range is empty, returns null in that cell's position. All non-null values are "JsonElement". Convert to desire.

##### Returns

_object[][]_ — 2 Dimensional array for each row/col values

---

### SetFormula

```csharp
Task SetFormula(string formula)
```

Set a formula in the cell.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|formula|string|All formulas begin with "="|

---

### SetFormula

```csharp
Task SetFormula(params string[][] formulas)
```

Set all formulas in the active range.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|formulas|string[][]|All formulas begin with "=". The size of each array must be the same number as the number of columns used|

---

### GetFormula

```csharp
Task<string> GetFormula()
```

Returns the formula in the cell. If there's not, return an empty string.

##### Returns

_string_ — Formula in the selected cell or empty

---

### GetFormulas

```csharp
Task<string[][]> GetFormulas()
```

Returns all formulas in the range. If a cell in the range doesn’t have a formula, returns an empty string in that cell's position.

##### Returns

_string[][]_ — 2D array of formulas or empty strings

---

### SetFontProperties

```csharp
Task SetFontProperties(UFontProperties properties)
```

Set font properties to the specified range.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|properties|[UFontProperties]({% link api/spreadsheets/data/styles/UFontProperties.md %})|Properties with null will not be applied (Don't use empty strings)|

---

### SetBorderStyle

```csharp
Task SetBorderStyle(EBorderType borderType, EBorderStyleType borderStyle, string color)
```

Set border to the range.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|borderType|[EBorderType]({% link api/spreadsheets/data/styles/EBorderType.md %})|Border Type to apply to the range|
|borderStyle|[EBorderStyleType](% link api/spreadsheets/data/styles/EBorderStyleType.md %)|Border Style to apply to the border's range|
|color|string|Color on hexadecimal ()|

---

### ResetStyle

```csharp
Task ResetStyle()
```

Sets all styles in the active range to default.

---

### GetStyles

```csharp
Task<UStyleData[][]> GetStyles()
```

Return all styles used in the active range. Be careful with getting a lot of styles. It may cause a StackOverflowException!

##### Returns

_[UStyleData]({% link api/spreadsheets/data/styles/UStyleData.md %})[][]_ — Matrix of style data for each cell

---

### SetHyperLink

```csharp
Task SetHyperLink(string text, string link)
```

Sets a hyper link in the first cell on the active range.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|text|string|Text for the Hyperlink|
|link|string|Link to redirect|

---

### SortAscending

```csharp
Task SortAscending(params int[] columns)
```

Sort selected range by ascending.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|columns|int[]|Columns to be sorted|

---

### SortAscending

```csharp
Task SortAscending(params (int column, bool ascending)[] sorts)
```

Sort selected range by ascending or descending.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|sorts|(int column, bool ascending)[]|Column to sort and ascending flag|

---

### Merge

```csharp
Task Merge(MergeStrategy strategy, bool defaultMerge)
```

Merge all cells in range.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|strategy|[MergeStrategy]({% link api/spreadsheets/data/styles/MergeStrategy.md %})|Strategy to merge all cells in range|
|defaultMerge|bool|True if the value in the upper left cell will be retained|

---

### BreakMerge

```csharp
Task BreakMerge()
```

Unmerge all cells in range.

---

### GetAllMerges

```csharp
Task<URange[]> GetAllMerges()
```

Get all merges in active page.

##### Returns

_[URange]({% link api/spreadsheets/data/workbook/URange.md %})[]_ — All merged ranges on the active page

---

### RangeIsPartOfMerge

```csharp
Task<bool> RangeIsPartOfMerge()
```

True if the range has cells that overlap a merged cell.

##### Returns

_bool_ — Whether any part of the range is merged

---

### CreateFilter

```csharp
Task CreateFilter()
```

Create a filter for the selected range (on the active page).

---

### HasFilter

```csharp
Task<bool> HasFilter()
```

Returns true if the active page has a filter on it.

##### Returns

_bool_ — Whether the page currently has a filter

---

### GetFilter

```csharp
Task<URange?> GetFilter()
```

Gets the range's filter for the active page.

##### Returns

_[URange]({% link api/spreadsheets/data/workbook/URange.md %})?_ — URange object with the range of the filter

---

### RemoveFilter

```csharp
Task RemoveFilter()
```

Removes the filter for the active page.

---

### AddConditionalFormat (active range)

```csharp
Task AddConditionalFormat(UConditionType type, UConditionFormatStyle style)
```

Adds a conditional format to the active page in the active range.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|type|[UConditionType]({% link api/spreadsheets/data/conditional-format/UConditionType.md %})|Condition under which the format will be applied|
|style|[UConditionFormatStyle]({% link api/spreadsheets/data/conditional-format/UConditionFormatStyle.md %})|The style that will be applied to the cells|

---

### AddConditionalFormat (specific ranges)

```csharp
Task AddConditionalFormat(UConditionType type, UConditionFormatStyle style, params URange[] ranges)
```

Adds a conditional format to the active page in the specified ranges.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|type|[UConditionType]({% link api/spreadsheets/data/conditional-format/UConditionType.md %})|Condition under which the format will be applied|
|style|[UConditionFormatStyle]({% link api/spreadsheets/data/conditional-format/UConditionFormatStyle.md %})|The style that will be applied to the cells|
|ranges|[URange]({% link api/spreadsheets/data/workbook/URange.md %})[]|Ranges where the conditional format will apply|

---

### DeleteConditionalFormat

```csharp
Task DeleteConditionalFormat(string idRule)
```

Deletes the specified conditional format by its ID.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|idRule|string|ID of the conditional format rule to delete|

---

### ClearConditionalFormats

```csharp
Task ClearConditionalFormats()
```

Clears all conditional formats in the page.

---

### GetAllConditionalFormats

```csharp
Task<UConditionalFormatRule[]> GetAllConditionalFormats()
```

Gets all conditional formats in the page.

##### Returns

_[UConditionalFormatRule]({% link api/spreadsheets/data/conditional-format/UConditionalFormatRule.md %})[]_ — Array of all conditional format rules on the page

---

### ApplyConditionalFormat

```csharp
Task ApplyConditionalFormat(string idRule, URange range)
```

Apply the rule with the given ID to the specified range.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|idRule|string|ID of the conditional format rule|
|range|[URange]({% link api/spreadsheets/data/workbook/URange.md %})|Range to which the rule will be applied|

---

### AddImage (active range)

```csharp
Task AddImage(string urlImage)
```

Sets an image in the active page at the active range.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|urlImage|string|URL or data URI of the image (JPEG, PNG, TIFF, GIF, ICO, SVG)|

---

### AddImage (custom position)

```csharp
Task AddImage(string urlImage, int row, int col, double? rowOffset = null, double? colOffset = null)
```

Inserts an image in the active page at a specific row and column.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|urlImage|string|URL or data URI of the image (JPEG, PNG, TIFF, GIF, ICO, SVG)|
|row|int|Row index|
|col|int|Column index|
|rowOffset|double?|Optional offset in the row position|
|colOffset|double?|Optional offset in the column position|

---

### AddImage (batch)

```csharp
Task AddImage(params UImage[] images)
```

Adds multiple images with custom properties to the active page.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|images|[UImage]({% link api/spreadsheets/data/images/UImage.md %})[]|Array of images to be added with all necessary metadata|

---

### GetImages

```csharp
Task<UImage[]> GetImages()
```

Gets all images on the active page.  
⚠️ Recommended only if the combined size is less than 33KB.

##### Returns

_[UImage]({% link api/spreadsheets/data/images/UImage.md %})[]_ — List of images on the page

---

### GetImagesId

```csharp
Task<string[]> GetImagesId()
```

Gets the IDs of all images on the active sheet.

##### Returns

_string[]_ — List of image IDs

---

### GetImage

```csharp
Task<UImage> GetImage(string id, bool withSource = true)
```

Gets an image by its ID from the active page.  
⚠️ Use `withSource: false` if the image is large (>33KB).

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|id|string|ID of the image|
|withSource|bool|Whether to include image source (data URI)|

##### Returns

_[UImage]({% link api/spreadsheets/data/images/UImage.md %})_ — Image data

---

### GetImageSource

```csharp
Task<string> GetImageSource(string id)
```

Gets the full data URI for the image, using chunking (safe for large images).

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|id|string|ID of the image|

##### Returns

_string_ — Data URI of the image

---

### DeleteImagesById

```csharp
Task DeleteImagesById(params string[] ids)
```

Removes selected images by their IDs from the active sheet.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|ids|string[]|IDs of images to delete|

---

### DeleteImages

```csharp
Task DeleteImages(params UImage[] images)
```

Removes the specified image objects from the active sheet.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|images|[UImage]({% link api/spreadsheets/data/images/UImage.md %})[]|Array of image objects to delete|

---

### InsertComment

```csharp
Task InsertComment(UniverComment comment)
```

Inserts a comment into the first cell in the active range.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|comment|[UniverComment]({% link api/generic/data/UniverComment.md %})|Comment data to insert|

---

### GetComment

```csharp
Task<UniverComment> GetComment(bool delete = false)
```

Gets the first comment in the first cell of the active range, optionally deletes it.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|delete|bool|Whether to delete the comment after retrieving it|

##### Returns

_[UniverComment]({% link api/generic/data/UniverComment.md %})_ — The retrieved comment

---

### GetComments

```csharp
Task<UniverComment[]> GetComments()
```

Gets all comments in the current sheet.

##### Returns

_[UniverComment]({% link api/generic/data/UniverComment.md %})[]_ — Array of all comments

---

### ClearComments

```csharp
Task ClearComments()
```

Deletes all comments on the active sheet.

---

### SetFreeze

```csharp
Task SetFreeze(int rows, int cols)
```

Freezes the specified number of rows and columns from the top-left (A1).

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|rows|int|Number of rows to freeze|
|cols|int|Number of columns to freeze|

----

### CancelFreeze

```csharp
Task CancelFreeze()
```

Cancels any frozen rows or columns in the active sheet.

---

### GetFreeze

```csharp
Task<UFreeze> GetFreeze()
```

Gets the current frozen rows and columns configuration.

##### Returns

_[UFreeze]({% link api/spreadsheets/data/workbook/UFreeze.md %})_ — The frozen state of the sheet

---

### GetRowsHeights

```csharp
Task<double[]> GetRowsHeights(params int[] rowPos)
```

Returns the height of each specified row.

##### Parameters

| Parameter | Type   | Description                 |
|-----------|--------|-----------------------------|
| rowPos    | int[]  | Indexes of the target rows  |

##### Returns

_double[]_ — Heights of the given rows

---

### GetColumnWidth

```csharp
Task<double[]> GetColumnWidth(params int[] colPos)
```

Returns the width of each specified column.

##### Parameters

| Parameter | Type   | Description                    |
|-----------|--------|--------------------------------|
| colPos    | int[]  | Indexes of the target columns  |

##### Returns

_double[]_ — Widths of the given columns

---

### SetColumnWidth

```csharp
Task SetColumnWidth(int colPos, double width)
```

Sets the width for a specific column.

##### Parameters

| Parameter | Type    | Description               |
|-----------|---------|---------------------------|
| colPos    | int     | Column index              |
| width     | double  | Desired column width      |

---

### SetRowHeight

```csharp
Task SetRowHeight(int rowPos, double height)
```

Sets the height for a specific row.

##### Parameters

| Parameter | Type    | Description             |
|-----------|---------|-------------------------|
| rowPos    | int     | Row index               |
| height    | double  | Desired row height      |

---

### InsertColumns

```csharp
Task InsertColumns(int colPos, int colCount = 1)
```

Inserts one or more blank columns starting at the specified position.

##### Parameters

| Parameter | Type | Description                                   |
|-----------|------|-----------------------------------------------|
| colPos    | int  | Starting index for the inserted columns       |
| colCount  | int  | Number of columns to insert (default is 1)    |

---

### DeleteColumns

```csharp
Task DeleteColumns(int colPos, int colCount = 1)
```

Deletes one or more columns starting at the specified position.

##### Parameters

| Parameter | Type | Description                                   |
|-----------|------|-----------------------------------------------|
| colPos    | int  | Starting index of the columns to delete       |
| colCount  | int  | Number of columns to delete (default is 1)    |

---

### InsertRows

```csharp
Task InsertRows(int rowPos, int rowCount = 1)
```

Inserts one or more blank rows starting at the specified position.

##### Parameters

| Parameter | Type | Description                                |
|-----------|------|--------------------------------------------|
| rowPos    | int  | Starting index for the inserted rows       |
| rowCount  | int  | Number of rows to insert (default is 1)    |

---

### DeleteRows

```csharp
Task DeleteRows(int rowPos, int rowCount = 1)
```

Deletes one or more rows starting at the specified position.

##### Parameters

| Parameter | Type | Description                              |
|-----------|------|------------------------------------------|
| rowPos    | int  | Starting index of the rows to delete     |
| rowCount  | int  | Number of rows to delete (default is 1)  |

---