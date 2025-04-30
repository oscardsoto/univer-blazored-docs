---
layout: page  
title: UniverInit
parent: Generic  
nav_order: 2
---

# UniverInit

Config object for UniverJS

```csharp
public struct UniverInit
```

## Remarks

Represents the initialization settings used by UniverJS to enable or disable specific features and behaviors on startup.

## Properties

| Name                      | Type    | Description                                                       |
|---------------------------|---------|-------------------------------------------------------------------|
| hasShort                  | bool    | Enable Short Preset (True by default).                            |
| hasDataValidation         | bool    | Enable DataValidation Preset (True by default).                   |
| hasFilter                 | bool    | Enable Filter Preset (True by default).                           |
| hasConditionalFormatting  | bool    | Enable Conditional Formats Preset (True by default).              |
| hasHyperLink              | bool    | Enable HyperLink Preset (True by default).                        |
| hasDrawing                | bool    | Enable drawing Preset (True by default).                          |
| hasThreadComment          | bool    | Enable Thread Comment Preset (True by default).                   |
| hasCrosshair              | bool    | Enable Crosshair Plugin (False by default).                       |
| hasWatermark              | bool    | Enable Watermark Plugin (False by default).                       |
| watermarkLabel            | string  | Text to show in the watermark of each sheet.                      |
| newSheetName              | string  | Name of the first sheet created after initialized.                |
| idDiv                     | string  | Id of the div that will execute Univer (default is uXlsxComp).    |

## Methods

### SetNewIdDiv

```csharp
public void SetNewIdDiv(string newId)
```

Sets the value for the div's Id to execute Univer.

##### Parameters

| Name    | Type   | Description                   |
|---------|--------|-------------------------------|
| newId   | string | New id to set for the div.    |

---