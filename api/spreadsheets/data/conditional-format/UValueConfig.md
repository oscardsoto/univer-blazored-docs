---
layout: page
title: UValueConfig
parent: Conditional Format
grand_parent: Data
nav_order: 17
---

# {{ page.title }}

IValueConfig, from Univer [See doc:](https://github.com/dream-num/univer/blob/dev/packages/sheets-conditional-formatting/src/models/type.ts#L30)

```csharp
public struct UValueConfig
```

## Remarks

Lorem Ipsum...

## Properties

|Property|Type|Description|
|---|---|---|
|type|string|ECFValueType value|
|value|object|Value to evaluate (in [JsonElement](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.jsonelement?view=net-9.0-pp) format, if extracted directly from Univer)|

## Constructors

```csharp
public UValueConfig()
```

IValueConfig, from Univer [See doc:](https://github.com/dream-num/univer/blob/dev/packages/sheets-conditional-formatting/src/models/type.ts#L30)

---------

```csharp
public UValueConfig(ECFValueType type, string value)
```

IValueConfig, from Univer [See doc:](https://github.com/dream-num/univer/blob/dev/packages/sheets-conditional-formatting/src/models/type.ts#L30)

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|type|[ECFValueType]({% link api/spreadsheets/data/conditional-format/ECFValueType.md %})|Value Type|
|value|string|Content for the value (string, or double only)|

---------

```csharp
public UValueConfig(ECFValueType type, double value)
```

IValueConfig, from Univer [See doc:](https://github.com/dream-num/univer/blob/dev/packages/sheets-conditional-formatting/src/models/type.ts#L30)

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|type|[ECFValueType]({% link api/spreadsheets/data/conditional-format/ECFValueType.md %})|Value Type|
|value|double|Content for the value (string, or double only)|

---------

## Methods

### SetType

```csharp
public void SetType(ECFValueType type)
```

Set "type" value from enum

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|type|[ECFValueType]({% link api/spreadsheets/data/conditional-format/ECFValueType.md %})|Value Type|

---------

### GetValueType

```csharp
public ECFValueType? GetValueType()
```

Returns the type value (in Enum)

##### Returns

[ECFValueType]({% link api/spreadsheets/data/conditional-format/ECFValueType.md %}) enum