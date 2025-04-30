---
layout: page
title: UIconSetConfig
parent: Conditional Format
grand_parent: Data
nav_order: 15
---

# {{ page.title }}

IIconSet "config" property, from Univer [See doc:](https://github.com/dream-num/univer/blob/dev/packages/sheets-conditional-formatting/src/models/type.ts#L96)

```csharp
public struct UIconSetConfig
```

## Remarks

Represents the configuration of a single icon within an IconSet conditional format. Includes the icon type, value, and evaluation operator.

## Properties

|Property|Type|Description|
|---|---|---|
|iconId|string|Icon Id (int in string value)|
|Operator|string|Operator value for the icon set ()|
|value|[UValueConfig]({% link api/spreadsheets/data/conditional-format/UValueConfig.md %})|Value to evaluate|
|iconType|string|Icon Type to show (Use SetIconType to change it correctly)|

## Constructors

```csharp
public UIconSetConfig()
```

IIconSet "config" property, from Univer [See doc:](https://github.com/dream-num/univer/blob/dev/packages/sheets-conditional-formatting/src/models/type.ts#L96)

---------

## Methods

### SetOperator

```csharp
public void SetOperator(ECFOperators op)
```

Set "operator" value via enum

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|op|[ECFOperators]({% link api/spreadsheets/data/conditional-format/ECFOperators.md %})|(No description provided)|

---------

### GetOperator

```csharp
public ECFOperators GetOperator()
```

Return the operator for the icon set (Enumerator)

##### Returns

[ECFOperators]({% link api/spreadsheets/data/conditional-format/ECFOperators.md %}): Parsed operator from string value

---------

### SetIconType

```csharp
public void SetIconType(EIconType icon)
```

Set "iconType" value via enum

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|icon|[EIconType]({% link api/spreadsheets/data/conditional-format/EIconType.md %})|(No description provided)|

---------

### GetIconType

```csharp
public EIconType? GetIconType()
```

Return the Icon Type (Enumerator)

##### Returns

[EIconType]({% link api/spreadsheets/data/conditional-format/EIconType.md %})?: Parsed icon type from string value