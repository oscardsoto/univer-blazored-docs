---
layout: page
title: UniverSpreadsheetJsInterop
parent: Services
grand_parent: Spreadsheets
nav_order: 3
---

# UniverSpreadsheetJsInterop

Interface that provides interoperability with Univer's spreadsheets and Blazor.

```csharp
public class UniverSpreadsheetJsInterop : IUniverJsInterop
```

## Remarks

The scoped acts as a bridge between Blazor and Univer spreadsheets via JavaScript interop. It dynamically loads JS libraries, queues actions, and resolves them using JS modules.

## Properties

| Property | Type | Description |
|---------|------|-------------|
| moduleTask | Lazy<`Task<IJSObjectReference>`> | Module to initialize Univer in the component |
| actionQueue | Queue<[UniverQueueValue]({% link api/generic/data/UniverQueueValue.md %})> | Action Queue for execution in FacadeAPI for Univer |

## Constructor

```csharp
public UniverSpreadsheetJsInterop(IJSRuntime runtime, IOptions<UniverConfig> options)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| runtime | IJSRuntime | JavaScript runtime from Blazor |
| options | IOptions<UniverConfig> | Configuration options for Univer |

## Methods

### InitializeAsync

```csharp
Task<bool> InitializeAsync(string newIdDiv)
```

Sets all instances of all scripts from Univer according to the version.

| Parameter | Type | Description |
|-----------|------|-------------|
| newIdDiv | string | The new Id for the div to execute Univer |

#### Returns

_`Task<bool>`_ — True if initialized correctly

---

### SetAction

```csharp
IUniverJsInterop SetAction(string action, params object[] args)
```

Sets an action for the FacadeAPI.

| Parameter | Type | Description |
|-----------|------|-------------|
| action | string | Method's name to execute on the Facade's API |
| args | object[] | Arguments for the method (must be serializable) |

#### Returns

[IUniverJsInterop]({& link api/generic/IUniverJsInterop.md &}) — Self, for chaining

---

### ResolveAsync

```csharp
Task ResolveAsync()
```

Resolves all queued actions through JS interop, throwing if any method cannot be found.

#### Returns

_Task_ — Completes when queue is processed

---

### ResolveAsync<T>

```csharp
Task<T> ResolveAsync<T>()
```

Resolves all queued actions and returns a typed result.

#### Returns

_`Task<T>`_ — Result from JavaScript execution

---

### GetUniverLinks

```csharp
string[] GetUniverLinks()
```

Returns all script components required by Univer based on the current config.

#### Returns

_string[]_ — Array of each Univer library URL to import

---

### ResolveActionAsync<T>

```csharp
Task<T> ResolveActionAsync<T>(string name, params object[] args)
```

Executes a direct method call in the JavaScript module and returns a result.

| Parameter | Type | Description |
|-----------|------|-------------|
| name | string | Name of the JavaScript function to call |
| args | object[] | Arguments to pass to the function |

#### Returns

_`Task<T>`_ — Return value from the JavaScript function

---

### ResolveActionAsync

```csharp
Task ResolveActionAsync(string name, params object[] args)
```

Executes a direct JavaScript method that does not return a value.

| Parameter | Type | Description |
|-----------|------|-------------|
| name | string | Name of the JavaScript function to call |
| args | object[] | Arguments to pass |

#### Returns

_Task_ — Completes when the JavaScript function finishes