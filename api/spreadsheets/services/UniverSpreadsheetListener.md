---
layout: page
title: UniverSpreadsheetListener
parent: Services
grand_parent: Spreadsheets
nav_order: 4
---

# UniverSpreadsheetListener

Univer Listener. A listener gets automatically the value of one cell every time its value has changed.

```csharp
public class UniverSpreadsheetListener : IUniverSpreadsheetListener
```

## Remarks

This class maintains a set of listeners for cell changes in Univer spreadsheets. It allows adding, removing, and invoking listeners through JavaScript interop.

## Properties

| Property | Type | Description |
|---------|------|-------------|
| Listeners | Dictionary<[UniverSpreadsheetListenerData]({% link api/spreadsheets/data/UniverSpreadsheetListenerData.md %}), `Action<object>`> | All active Listeners |

## Constructor

```csharp
public UniverSpreadsheetListener(IUniverJsInterop univerJS)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| univerJS | IUniverJsInterop | Univer's Interop to access Univer |

## Methods

### InitializeListenersAsync

```csharp
void InitializeListenersAsync()
```

Initializes the listener dictionary and sets up the JSInterop reference.

---

### AddListenerAsync

```csharp
void AddListenerAsync(UniverSpreadsheetListenerData data, Action<object> _event)
```

Adds a new listener to the dictionary and binds it via JSInterop.

| Parameter | Type | Description |
|-----------|------|-------------|
| data | [UniverSpreadsheetListenerData]({% link api/spreadsheets/data/UniverSpreadsheetListenerData.md %}) | Data to locate the listener in the workbook |
| _event | `Action<object>` | Callback that triggers when the cell value changes |

---

### RemoveListenerAsync

```csharp
void RemoveListenerAsync(UniverSpreadsheetListenerData data)
```

Removes a listener both from JSInterop and the local dictionary.

| Parameter | Type | Description |
|-----------|------|-------------|
| data | [UniverSpreadsheetListenerData]({% link api/spreadsheets/data/UniverSpreadsheetListenerData.md %}) | Listener to remove |

---

### GetListeners

```csharp
UniverSpreadsheetListenerData[] GetListeners()
```

Returns all currently active listeners.

#### Returns

[UniverSpreadsheetListenerData]({% link api/spreadsheets/data/UniverSpreadsheetListenerData.md %})[] — Array of keys representing active listeners

---

### OnDataChanged

```csharp
void OnDataChanged(UniverSpreadsheetListenerData data, object value)
```

JSInvokable method that triggers the appropriate callback when a cell value is updated via JS.

| Parameter | Type | Description |
|-----------|------|-------------|
| data | [UniverSpreadsheetListenerData]({% link api/spreadsheets/data/UniverSpreadsheetListenerData.md %}) | The listener's identifier |
| value | object | The new value from the cell |