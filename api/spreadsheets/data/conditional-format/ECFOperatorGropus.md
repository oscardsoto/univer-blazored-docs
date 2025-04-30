---
layout: page
title: ECFOperatorGroups
obj_name: ECFOperatorGropus
parent: Conditional Format
grand_parent: Data
nav_order: 2
---

# {{ page.title }}

Groups for operators that correspond to each Text, Dates and Numbers

```csharp
public static class ECFOperatorGropus
```

# Attributes

## {{ page.obj_name }}.TextOperators

CFTextOperator, from Univer [See doc](https://github.com/dream-num/univer/blob/dev/packages/sheets-conditional-formatting/src/base/const.ts#L20)

### Syntax

```csharp
public static ECFOperators TextOperators
```

|Values|
|---|
|ECFOperators.beginsWith|
|ECFOperators.endsWith|
|ECFOperators.containsText|
|ECFOperators.notContainsText|
|ECFOperators.equal|
|ECFOperators.notEqual|
|ECFOperators.containsBlanks|
|ECFOperators.notContainsBlanks|
|ECFOperators.containsErrors|
|ECFOperators.notContainsErrors|

## {{ page.obj_name }}.TimePeriodOperators

CFTimePeriodOperator, from Univer [See doc:](https://github.com/dream-num/univer/blob/dev/packages/sheets-conditional-formatting/src/base/const.ts#L32)

### Syntax

```csharp
public static ECFOperators TimePeriodOperators
```

|Values|
|---|
|ECFOperators.today|
|ECFOperators.yesterday|
|ECFOperators.tomorrow|
|ECFOperators.last7Days|
|ECFOperators.thisMonth|
|ECFOperators.lastMonth|
|ECFOperators.nextMonth|
|ECFOperators.thisWeek|
|ECFOperators.lastWeek|
|ECFOperators.nextWeek|

## {{ page.obj_name }}.NumberOperators

CFNumberOperator, from Univer [See doc:](https://github.com/dream-num/univer/blob/dev/packages/sheets-conditional-formatting/src/base/const.ts#L44)

### Syntax

```csharp
public static ECFOperators NumberOperators
```

|Values|
|---|
|ECFOperators.greaterThan|
|ECFOperators.lessThan|
|ECFOperators.greaterThanOrEqual|
|ECFOperators.lessThanOrEqual|
|ECFOperators.notBetween|
|ECFOperators.between|
|ECFOperators.equal|
|ECFOperators.notEqual|

# Remarks

