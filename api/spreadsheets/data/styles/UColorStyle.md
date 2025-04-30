---
layout: page
title: UColorStyle
parent: Styles
grand_parent: Data
nav_order: 11
---

# {{ page.title }}

UColorStyle, from Univer [See doc](https://univer.ai/typedoc/@univerjs/core/interfaces/IColorStyle)

```csharp
public struct UColorStyle
```

## Remarks

Defines a color style in Univer, allowing specification of either a direct RGB color or a reference to a theme-based color.

## Properties

| Property | Type       | Description                                                                 |
|----------|------------|-----------------------------------------------------------------------------|
| rgb      | string     | RGB color defined as a hexadecimal string.                                  |
| th       | int?       | Optional theme index. If present, determines if a theme color should apply. |