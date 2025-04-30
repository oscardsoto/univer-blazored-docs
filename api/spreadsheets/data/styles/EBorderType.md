---
layout: page
title: EBorderType
parent: Styles
grand_parent: Data
nav_order: 2
---

# {{ page.title }}

BorderType enum, from Univer's object BorderData, to specify in which border the changes will apply [See doc: ](https://univer.ai/typedoc/@univerjs/core/interfaces/IBorderData)

```csharp
public enum EBorderType
```

## Fields

|Name|Value|Descrpition|
|---|---|---|
|ALL|0|All borders|
|BLTR|1|Bottom-Left, Top-Right|
|BOTTOM|2|Bottom border|
|HORIZONTAL|3|All horizontal borders for the range|
|INSIDE|4|All borders inside the range|
|LEFT|5|All borders from the left for the range|
|MLTR_BCTR|6|Middle-Left Top-Right, Bottom-Center Top-Right|
|NONE|7|No borders|
|OUTSIDE|8|All borders outside the range|
|RIGHT|9|All borders from the right for the page|
|TLBC_TLMR|10|Top-Left Bottom-Center, Top-Left Middle-Right|
|TLBR|11|Top-Left Bottom-Right|
|TLBR_TLBC_TLMR|12|Top-Left Bottom-Right, Top-Left Bottom-Center, Top-Left Middle-Right|
|TOP|13|All top borders from the range|
|VERTICAL|14|All vertical borders for the range|

## Remarks
This enum is used to indicate which border(s) a specific style should be applied to in Univer's spreadsheet system. It allows granular styling for different edges and corners of cell ranges.