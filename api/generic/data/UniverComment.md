---
layout: page
title: UniverComment
parent: Data
grand_parent: Generic
nav_order: 1
---

# {{ page.title }}

Univer Thread Comment component's data

```csharp
public class UniverComment
```

## Remarks

Lorem ipsum...

## Properties

|Property|Type|Description|
|---|---|---|
|unitId|string|Workbook Id|
|subUnitId|string|Worksheet Id|
|threadId|string|Thread Id|
|dT|string|DateTime (as string) when the comment was created|
|personId|string|User's Id that create the commment|
|reference|string|Location in cell in A1 notation|
|text|[URichTextValue]({% link api/spreadsheets/data/rich-text/URichTextValue.md %})|Comment's content|

## Constructors

```csharp
public UniverComment()
```

Univer Thread Comment component's data

---------

## Methods

### SetText

```csharp
public void SetText(string text)
```

Sets a plain text in the comment

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|text|string|Sets a plain text in the comment|

---------

### SetDateTime

```csharp
public void SetDateTime(DateTime? dt = null)
```

Sets the DateTime for the comment

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|dt|DateTime?|Date for the comment (leave null if the Date is Now)|