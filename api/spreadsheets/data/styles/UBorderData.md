---
layout: page
title: UBorderData
parent: Styles
grand_parent: Data
nav_order: 9
---

# {{ page.title }}

UBorderData, from Univer [See doc](https://univer.ai/typedoc/@univerjs/core/interfaces/IBorderData)

```csharp
public struct UBorderData
```

## Remarks

Defines the structure of border data for a cell or text element in Univer. Each property corresponds to a possible edge or diagonal where a border style can be applied.

## Properties

|Property|Type|Description|
|---|---|---|
|b|[UBorderStyleData]({% link api/spreadsheets/data/styles/UBorderStyleData.md %})?|Bottom border|
|bc_tr|[UBorderStyleData]({% link api/spreadsheets/data/styles/UBorderStyleData.md %})?|START_BOTTOM_CENTER_END_TOP_RIGHT|
|bl_tr|[UBorderStyleData]({% link api/spreadsheets/data/styles/UBorderStyleData.md %})?|START_BOTTOM_LEFT_END_TOP_RIGHT|
|l|[UBorderStyleData]({% link api/spreadsheets/data/styles/UBorderStyleData.md %})?|Left border|
|ml_tr|[UBorderStyleData]({% link api/spreadsheets/data/styles/UBorderStyleData.md %})?|START_MIDDLE_LEFT_END_TOP_RIGHT|
|r|[UBorderStyleData]({% link api/spreadsheets/data/styles/UBorderStyleData.md %})?|Right border|
|t|[UBorderStyleData]({% link api/spreadsheets/data/styles/UBorderStyleData.md %})?|Top border|
|tl_bc|[UBorderStyleData]({% link api/spreadsheets/data/styles/UBorderStyleData.md %})?|START_TOP_LEFT_END_BOTTOM_CENTER|
|tl_br|[UBorderStyleData]({% link api/spreadsheets/data/styles/UBorderStyleData.md %})?|START_TOP_LEFT_END_BOTTOM_RIGHT|
|tl_mr|[UBorderStyleData]({% link api/spreadsheets/data/styles/UBorderStyleData.md %})?|START_MIDDLE_LEFT_END_TOP_RIGHT|