---
layout: page
title: URange
parent: Workbook
grand_parent: Data
nav_order: 2
---

# {{ page.title }}

IRange, from Univer. [See doc:](https://univer.ai/typedoc/@univerjs/core/interfaces/IRange)

```csharp
public struct URange
```

## Remarks

Represents a range of cells in a spreadsheet, including support for A1 notation parsing and conversion.

## Properties

|Property|Type|Description|
|---|---|---|
|startRow|int|The start row (inclusive) of the range startRow|
|endRow|int|The end row (exclusive) of the range endRow|
|startColumn|int|The start column (inclusive) of the range startColumn|
|endColumn|int|The end column (exclusive) of the range endColumn|

## Constructors

```csharp
public URange()
```

IRange, from Univer. [See doc:](https://univer.ai/typedoc/@univerjs/core/interfaces/IRange)

---------

```csharp
public URange(int row, int col)
```

IRange, from Univer. [See doc:](https://univer.ai/typedoc/@univerjs/core/interfaces/IRange)

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|row|int|Cell's row|
|col|int|Cell's column|

---------

```csharp
public URange(int startRow, int endRow, int startColumn, int endColumn)
```

IRange, from Univer. [See doc:](https://univer.ai/typedoc/@univerjs/core/interfaces/IRange)

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|startRow|int|First row of the range|
|endRow|int|Last row of the range|
|startColumn|int|First column of the range|
|endColumn|int|Last column of the range|

---------

```csharp
public URange(string a1Notation)
```

IRange, from Univer. [See doc:](https://univer.ai/typedoc/@univerjs/core/interfaces/IRange)

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|a1Notation|string|A1 Notattion for the range/cell|

---------

## Methods

### GetFirstCellOfRange

```csharp
public URange GetFirstCellOfRange()
```

Returns the first cell of this range

##### Returns

URange: A new URange instance with the first cell

---------

### GetLastCellOfRange

```csharp
public URange GetLastCellOfRange()
```

Returns the last cell of this range

##### Returns

URange: A new URange instance with the last cell

---------

### ToA1Notation

```csharp
public string ToA1Notation()
```

Returns this range as a A1 notation

##### Returns

string: A1 notation of the current range