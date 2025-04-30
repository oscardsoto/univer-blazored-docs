---
layout: page
title: UTextRotation
parent: Styles
grand_parent: Data
nav_order: 21
---

# {{ page.title }}

ITextRotation, from Univer  
See doc: [Univer TypeDoc - ITextRotation](https://univer.ai/typedoc/@univerjs/core/interfaces/ITextRotation)

```csharp
public struct UTextRotation
```

## Remarks

Defines the rotation configuration for cell text. Rotation can be angled or vertical.

## Properties

| Property | Type | Default | Description |
|----------|------|---------|-------------|
| a        | int  | 0       | Angle of text rotation, in degrees |
| v        | int  | 0       | Whether the text is vertical (0: no, 1: yes) |