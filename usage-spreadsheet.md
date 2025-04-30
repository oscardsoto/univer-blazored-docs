---
title: Spreadsheet Usage & Tips
layout: home
parent: Get Started
nav_order: 1
permalink: /spreadsheet-usage/
---
# {{ page.title }}
{: .no_toc }

This section contains all information about how to get an set information in the spreadsheet controller of Univer Blazored with the Agent.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Univer Agent

The next list of methods are used to get or set information in the spreadsheet.

### Sheet operations

- `SetActiveRange(URange range)` - Sets the range to work in the active sheet on the component.
- `GetSheetsInfo()` - Return all sheets information.
- `AddNewSheet(string sheetName, int rows, int cols, string hexColorTab = null)` - Adds a new Worksheet in the active workbook.
- `DeleteSheet(string idSheet = null)` - Removes the specified sheet.

### Data

- `SetValue(object value)` - Set a value on a specific Row/Col.
- `GetValue<TValue>()` - Gets the value in the specific Row/col. If not, return null.
- `SetValue(params object[][] values)` - Set values on a range.
- `GetValues()` - Gets all values in the range. If a cell in the range is empty, returns null in that cell's position.

### Formulas

- `SetFormula(string formula)` - Set a formula in the cell.
- `SetFormula(params string[][] formulas)` - Set all formulas in the active range.
- `GetFormula()` - Returns the formula in the cell. If there's not, return an empty string.
- `GetFormulas()` - Returns all formulas in the range.

### Styles

- `SetFontProperties(properties)` - Set font properties to the specified range.
- `SetBorderStyle(borderType, borderStyle, color)` - Set border to the range.
- `ResetStyle()` - Sets all styles in the active range to default.
- `GetStyles()` - Return all styles used in the active range.
- `SetHyperLink(text, link)` - Sets a hyper link in the first cell on the active range.

### Sorting

- `SortAscending(columns)` - Sort selected range by ascending.
- `SortAscending(sorts)` - Sort selected range by ascending or descending.

### Merge

- `Merge(strategy, defaultMerge)` - Merge all cells in range.
- `BreakMerge()` - Unmerge all cells in range.
- `GetAllMerges()` - Get all merges in active page.
- `RangeIsPartOfMerge()` - True if the range has cells that overlap a merged cell.

### Filters

- `CreateFilter()` - Create a filter for the selected range (on the active page).
- `HasFilter()` - Returns true if the active page has a filter on it.
- `GetFilter()` - Gets the range's filter for the active page.
- `RemoveFilter()` - Removes the filter for the active page.

### Conditional Formats

- `AddConditionalFormat(type, style)` - Adds a conditional format to the active page in the active range.
- `AddConditionalFormat(type, style, ranges)` - Adds a conditional format to the active page in the specified ranges.
- `DeleteConditionalFormat(idRule)` - Deletes the specified conditional format by its ID.
- `ClearConditionalFormats()` - Clears all conditional formats in the page.
- `GetAllConditionalFormats()` - Gets all conditional formats in the page.
- `ApplyConditionalFormat(idRule, range)` - Apply the rule with the given ID to the specified range.

### Images

- `AddImage(urlImage)` - Sets an image in the active page at the active range.
- `AddImage(urlImage, row, col, rowOffset = null, colOffset = null)` - Inserts an image in the active page at a specific row and column.
- `AddImage(images)` - Adds multiple images with custom properties to the active page.
- `GetImages()` - Gets all images on the active page.
- `GetImagesId()` - Gets the IDs of all images on the active sheet.
- `GetImage(id, withSource = true)` - Gets an image by its ID from the active page.
- `GetImageSource(id)` - Gets the full data URI for the image, using chunking (safe for large images).
- `DeleteImagesById(ids)` - Removes selected images by their IDs from the active sheet.
- `DeleteImages(images)` - Removes the specified image objects from the active sheet.

### Comments

- `InsertComment(comment)` - Inserts a comment into the first cell in the active range.
- `GetComment(delete = false)` - Gets the first comment in the first cell of the active range, optionally deletes it.
- `GetComments()` - Gets all comments in the current sheet.
- `ClearComments()` - Deletes all comments on the active sheet.

### Freeze rows and columns

- `SetFreeze(rows, cols)` - Freezes the specified number of rows and columns from the top-left (A1).
- `CancelFreeze()` - Cancels any frozen rows or columns in the active sheet.
- `GetFreeze()` - Gets the current frozen rows and columns configuration.

### Row/Column management

- `GetRowsHeights(rowPos)` - Returns the height of each specified row.
- `GetColumnWidth(colPos)` - Returns the width of each specified column.
- `SetColumnWidth(colPos, width)` - Sets the width for a specific column.
- `SetRowHeight(rowPos, height)` - Sets the height for a specific row.
- `InsertColumns(colPos, colCount = 1)` - Inserts one or more blank columns starting at the specified position.
- `DeleteColumns(colPos, colCount = 1)` - Deletes one or more columns starting at the specified position.
- `InsertRows(rowPos, rowCount = 1)` - Inserts one or more blank rows starting at the specified position.
- `DeleteRows(rowPos, rowCount = 1)` - Deletes one or more rows starting at the specified position.