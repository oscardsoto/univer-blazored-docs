---
layout: page
title: UConditionalFormatRule
parent: Conditional Format
grand_parent: Data
nav_order: 10
---

# UConditionalFormatRule

IConditionlFormattingRule, from Univer [See doc:](https://github.com/dream-num/univer/blob/dev/packages/sheets-conditional-formatting/src/models/type.ts)

```csharp
public struct UConditionalFormatRule
```

## Remarks

Represents a conditional formatting rule in a spreadsheet, encapsulating the rule configuration and metadata such as range, ID, and behavior flags. The rule itself is stored as a JSON object to enable flexible deserialization of various conditional format types (e.g., HighlightCell, DataBar, etc).

## Properties

| Property     | Type             | Description |
|--------------|------------------|-------------|
| ranges       | List<URange>     | Ranges to apply the conditional format |
| cfId         | string           | Id for the conditional format |
| stopIfTrue   | bool             | True if only apply to 1 element to stop |
| rule         | [JsonObject](https://learn.microsoft.com/en-us/dotnet/api/system.text.json.nodes.jsonobject?view=net-9.0-pp)       | Rule object for the conditional format. See doc for every single combination (This is serialized as a JsonObject to reduce code) |

## Methods

### GetTypeConditionalFormat

```csharp
public ECFRuleType? GetTypeConditionalFormat()
```

Returns the type of conditional format inside "rule" JsonObject. Returns null if *rule* or the "type" key doesn't exist.

##### Returns:
[ECFRuleType]({% link api/spreadsheets/data/conditional-format/ECFRuleType.md %})? — Type of conditional format as enum

---

### GetSubType

```csharp
public ECFSubRuleType? GetSubType()
```

Returns the SubType of the conditional format inside "rule" JsonObject. Only applicable for "highlightCell" type.

##### Returns:
[ECFSubRuleType](% link api/spreadsheets/data/conditional-format/ECFSubRuleType.md %)? — Subtype for highlightCell conditional format

---

### GetOperator

```csharp
public ECFOperators? GetOperator()
```

Returns the operator at the root node in "rule" JsonObject. Only applicable for "highlightCell" type and: "text", "timePeriod", "number" and "average" SubTypes.

##### Returns:
[ECFOperators]({% link api/spreadsheets/data/conditional-format/ECFOperators.md %})? — Operator used in the conditional rule

---

### GetStyleUsed

```csharp
public IStyleBase? GetStyleUsed()
```

Returns the style object at the root node in "rule" JsonObject. Only applicable for "highlightCell" type.

##### Returns:
[IStyleBase]({% link api/spreadsheets/data/styles/IStyleBase.md %})? — Style object applied to the conditional format

---

### GetDataBarConfig

```csharp
public UDataBarConfig? GetDataBarConfig()
```

Returns the configuration object for the Data Bar Conditional Format. Only applicable for "dataBar" type.

##### Returns:
[UDataBarConfig]({% link api/spreadsheets/data/conditional-format/UDataBarConfig.md %})? — DataBar configuration object

---

### GetColorScaleConfigs

```csharp
public UColorScaleConfig[] GetColorScaleConfigs()
```

Returns the configuration object for the Color Scale Conditional Format. Only applicable for "colorScale" type.

##### Returns:
[UColorScaleConfig]({% link api/spreadsheets/data/conditional-format/UColorScaleConfig.md %})[] — Color scale configuration array

---

### GetIconSetConfigs

```csharp
public UIconSetConfig[] GetIconSetConfigs()
```

Returns the configuration object for the Icon Set Conditional Format. Only applicable for "iconSet" type.

##### Returns:
[UIconSetConfig]({% link api/spreadsheets/data/conditional-format/UIconSetConfig.md %})[] — Icon set configuration array