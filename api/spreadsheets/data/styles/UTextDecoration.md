---
layout: page
title: UTextDecoration
parent: Styles
grand_parent: Data
nav_order: 20
---

# {{ page.title }}

ITextDecoration, from Univer  
See doc: [Univer TypeDoc - ITextDecoration](https://univer.ai/typedoc/@univerjs/core/interfaces/ITextDecoration)

```csharp
public struct UTextDecoration
```

## Remarks

Represents styling information for text decoration such as underline, strikethrough, or overline. Used in various style definitions across cells.

## Properties

| Property | Type | Default | Description |
|----------|------|---------|-------------|
| c        | int?           | null | Follow the font color. If true, `cl` does not take effect |
| cl       | [UColorStyle]({% link api/spreadsheets/data/styles/UColorStyle.md %})?   | null | Line color |
| s        | int            | 0    | Show the line (0: false, 1: true) |
| t        | [UTextDecoration]({% link api/spreadsheets/data/styles/UTextDecoration.md %})? | null | Line type (e.g., underline, strikethrough, overline) |