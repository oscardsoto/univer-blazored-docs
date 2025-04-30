---
layout: page
title: IUniverSpreadsheetListener
parent: Services
grand_parent: Spreadsheets
nav_order: 1
---

# {{ page.title }}

Univer Listener. A listener gets automatically the value of one cell every time its value has changed

```csharp
public interface IUniverSpreadsheetListener
```

## Remarks

This interface defines a contract for spreadsheet listeners that react to changes in individual cell values.
It manages the lifecycle and interaction of listeners via JavaScript interop.


Any Scoped service that manage Spreadsheet Listeners must use this contract in order to work correctly in the Javascript environment.

## Properties

|Property|Type|Description|
|---|---|---|
|Listeners|Dictionary<[UniverSpreadsheetListenerData]({% link api/spreadsheets/data/UniverSpreadsheetListenerData.md %}), Action<object>>|All active Listeners|

## Methods

### InitializeListenersAsync

```csharp
void InitializeListenersAsync()
```

Init the dictionary and the relation in the JSInterop

---------

### AddListenerAsync

```csharp
void AddListenerAsync(UniverSpreadsheetListenerData data, Action<object> _event)
```

Adds a new listener to the array

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|data|[UniverSpreadsheetListenerData]({% link api/spreadsheets/data/UniverSpreadsheetListenerData.md %})|Data to locate the listener in the workbook|
|_event|`Action<object>`|Triggers when the cell in the listener change its value|

---------

### RemoveListenerAsync

```csharp
void RemoveListenerAsync(UniverSpreadsheetListenerData data)
```

Removes the specified listener in the array

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|data|[UniverSpreadsheetListenerData]({% link api/spreadsheets/data/UniverSpreadsheetListenerData.md %})|Item to delete|

---------

### GetListeners

```csharp
UniverSpreadsheetListenerData[] GetListeners()
```

Returns all active listeners

##### Returns

[UniverSpreadsheetListenerData]({% link api/spreadsheets/data/UniverSpreadsheetListenerData.md %})[]: Array of all currently active listeners

---------

### OnDataChanged

```csharp
void OnDataChanged(UniverSpreadsheetListenerData data, object value)
```

JSInvokable: Event for the Manager to trigger the listener, depending the cell that was value changed

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|data|[UniverSpreadsheetListenerData]({% link api/spreadsheets/data/UniverSpreadsheetListenerData.md %})|Data Listener|
|value|object|Value obtained|