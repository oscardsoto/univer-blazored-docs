---
layout: page
title: EWrapStrategy
parent: Styles
grand_parent: Data
nav_order: 7
---

# {{ page.title }}

WrapStrategy, from Univer [See doc: ](https://univer.ai/typedoc/@univerjs/core/enumerations/WrapStrategy)

```csharp
public enum EWrapStrategy
```

## Fields

| Name        | Value | Description                                  |
|-------------|-------|----------------------------------------------|
| UNSPECIFIED | 0     | Context dependent.                           |
| OVERFLOW    | 1     | Not cut text at the end of the cell.         |
| CLIP        | 2     | Cut the text at the end of the cell.         |
| WRAP        | 3     | Just wrap the text within the cell.          |

## Remarks
This enum defines the text wrapping behavior for a cell in Univer. It can be context-dependent, wrap the text, cut it off, or allow the text to overflow beyond the cell boundary.