---
layout: page
title: EIconType
parent: Conditional Format
grand_parent: Data
nav_order: 6
---

# {{ page.title }}

IIconType, from Univer [See doc:](https://github.com/dream-num/univer/blob/dev/packages/sheets-conditional-formatting/src/models/icon-map.ts)  
(Every enum starts with "I_", but will be replaced with empty on declaration)

```csharp
public enum EIconType
```

## Fields

|Name|Value|Descrpition|
|---|---|---|
|I_3Arrows|0|Represents three-arrow formatting icon.|
|I_3ArrowsGray|1|Represents a gray three-arrow formatting icon.|
|I_4Arrows|2|Represents four-arrow formatting icon.|
|I_4ArrowsGray|3|Represents a gray four-arrow formatting icon.|
|I_5Arrows|4|Represents five-arrow formatting icon.|
|I_5ArrowsGray|5|Represents a gray five-arrow formatting icon.|
|I_3Triangles|6|Represents a gray three-triangle formatting icon.|
|I_4RedToBlack|7|Represents a red to black traffic light symbol.|
|I_3TrafficLights1|8|Represents a traffic light symbol with one red and two yellow lights.|
|I_3TrafficLights2|9|Represents a traffic light symbol with two red lights and one green light.|
|I_3Signs|10|Represents three sign symbols formatting icon (i.e., signs or marks).|
|I__5Felling|11|Represents five shading or felling symbols formatting icon.|
|I_4TrafficLights|12|Represents four traffic lights symbol.|
|I_3Symbols|13|Represents three symbols formatting icon.|
|I_3Symbols2|14|Represents another three symbols formatting icon.|
|I_3Flags|15|Represents a flag symbol.|
|I_4Rating|16|Represents four rating symbols formatting icon.|
|I_5Rating|17|Represents five rating symbols formatting icon.|
|I_5Quarters|18|Represents a five-quarter symbol (i.e., quarter marks).|
|I_5Felling|19|Represents five felling or shading symbols formatting icon.|
|I_5Boxes|20|Represents a box symbol.|
|I_3Stars|21|Represents three stars formatting icon.|

## Remarks
This enum defines the different types of icon set formatting options available in Univer's conditional formatting system. Enum members start with "I_" as a convention from the original source but are stripped upon usage in rendering.