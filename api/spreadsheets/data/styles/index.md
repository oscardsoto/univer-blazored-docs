---
layout: page
title: Styles
parent: Data
grand_parent: Spreadsheets
---
# Namespace
## UniverBlazored.{{ page.grand_parent }}.{{page.parent}}.{{page.title}}

## Remarks

This namespace contains all data used in Univer to manage styles inside the UI, from cell style to the text style (excluding rich text, wich will be managed in [its namespace]({% link api/spreadsheets/data/rich-text/index.md %})).

Most of the enums and classes enlisted here are similar (or equal) interfaces and classes from Univer's original API.

## Important notes
- An object with an "E" or "F" at the beginning indicates an Enumerator (except MergeStartegy)
- An object with an "U" at the beginning indicates a Class or a Struct

## Example

A style can be directly applied with the [Agent]({% link api/spreadsheets/services/UniverSpreadsheetAgent.md %}), and after the style is extracted:

```csharp
await agent.SetActiveRange(range);
var styles = await agent.GetStyles();

UStyleData posData = styles[0][0];
posData.ff  // Font Family
posData.fs  // Font size
posData.it  // Italic (0 for false)
...
```