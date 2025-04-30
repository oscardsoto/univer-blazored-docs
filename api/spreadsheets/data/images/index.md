---
layout: page
title: Images
parent: Data
grand_parent: Spreadsheets
---
# Namespace
## UniverBlazored.{{ page.grand_parent }}.{{page.parent}}.{{page.title}}

## Remarks

This namespace contains all data used in Univer to manage images inside the UI.

Most of the enums and classes enlisted here are similar (or equal) interfaces and classes from Univer's original API.

## Important notes
- An object with an "E" at the beginning indicates an Enumerator
- An object with an "U" at the beginning indicates a Class or a Struct

## Example

You can get the information of an image though [Agent]({% link api/spreadsheets/services/UniverSpreadsheetAgent.md %}), and use it:

```csharp
var imagesId = await agent.GetImagesId();
foreach (var imgId in imagesId)
{
    var imageInfo = await agent.GetImage(imgId, false);
    ...
    imageInfo.source = await agent.GetImageSource(imgId);
    // DO something with the info...
}
```