---
layout: page
title: UAverageHighlightCell
parent: Conditional Format
grand_parent: Data
nav_order: 7
---

# {{ page.title }}

IAverageHighlightCell, from Univer [See doc:](https://github.com/dream-num/univer/blob/dev/packages/sheets-conditional-formatting/src/models/type.ts#L74)

```csharp
public struct UAverageHighlightCell
```

## Remarks

Represents a conditional formatting configuration that highlights cells based on average values using a specific style and operator.

## Properties

|Property|Type|Description|
|---|---|---|
|type|string|[ECFRuleType]({% link api/spreadsheets/data/conditional-format/ECFRuleType.md %}) value|
|subType|string|[ECFSubRuleType]({% link api/spreadsheets/data/conditional-format/ECFSubRuleType.md %}) value|
|style|[IStyleBase]({% link api/spreadsheets/data/styles/IStyleBase.md %})|Style applied|
|Operator|string|[ECFOperators]({% link api/spreadsheets/data/conditional-format/ECFOperators.md %}) value|

## Constructors

```csharp
public UAverageHighlightCell()
```

IAverageHighlightCell, from Univer [See doc:](https://github.com/dream-num/univer/blob/dev/packages/sheets-conditional-formatting/src/models/type.ts#L74)

---------

## Methods

### SetOperator

```csharp
public void SetOperator(ECFOperators op)
```

Set "operator" value from enum

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|op|[ECFOperators]({% link api/spreadsheets/data/conditional-format/ECFOperators.md %})|Operator to assign if valid as a number operator|