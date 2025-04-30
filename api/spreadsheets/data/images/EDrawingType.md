---
layout: page
title: EDrawingType
parent: Images
grand_parent: Data
nav_order: 1
---

# {{ page.title }}

DrawingTypeEnum, from Univer [see doc:](https://github.com/dream-num/univer/blob/dev/packages/core/src/types/interfaces/i-document-data.ts)

```csharp
public enum EDrawingType
```

## Fields

|Name|Value|Descrpition|
|---|---|---|
|UNRECOGNIZED|-1|The drawing type is unrecognized or undefined.|
|DRAWING_IMAGE|0|Represents an image. This could be a picture, logo, etc.|
|DRAWING_SHAPE|1|Represents a shape like rectangle, circle, triangle, etc.|
|DRAWING_CHART|2|Represents a chart type object (like bar graph, line graph, pie chart, etc).|
|DRAWING_TABLE|3|Represents a table. This could be a grid of data points.|
|DRAWING_SMART_ART|4|Represents a smart art object (like a sparkline).|
|DRAWING_VIDEO|5|Represents a video file. This could be an embedded youtube video link or similar.|
|DRAWING_GROUP|6|Represents a group of other drawings, could be a layer or a grouped element.|
|DRAWING_UNIT|7|Represents a unit of measure in the drawing. Could be millimeter, centimeter, inch etc.|
|DRAWING_DOM|8| |

## Remarks
This enum defines the different types of drawable elements within Univer, including images, shapes, charts, videos, and grouping mechanisms.