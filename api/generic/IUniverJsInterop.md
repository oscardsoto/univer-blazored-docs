---
layout: page
title: IUniverJsInterop
parent: Generic
nav_order: 4
---

# {{ page.title }}

Interface that provides interoperability with Univer and Blazor.

```csharp
public interface IUniverJsInterop
```

## Remarks

This interface facilitates the interaction between Univer's JavaScript environment and Blazor components by providing script initialization, queuing API calls, and executing JavaScript functions with or without return values.

Every single component that connects to Blazor (Spreadsheets, Documents and Presentations) require this Interface to get/set the data correctly.

## Properties

|Property|Type|Description|
|---|---|---|
|moduleTask|Lazy<Task<IJSObjectReference>>|Module to initialize Univer in the component|
|actionQueue|Queue<UniverQueueValue>|Action Queue for execute in FacadeAPI for Univer|

## Methods

### InitializeAsync

```csharp
Task<bool> InitializeAsync(string newIdDiv)
```

Sets all instances of all scripts from Univer according to the version

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|newIdDiv|string|The new Id for the div to execute Univer|

##### Returns

`Task<bool>`: True if initialization is successful

---------

### SetAction

```csharp
IUniverJsInterop SetAction(string action, params object[] args)
```

Sets an action for the FacadeAPI

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|action|string|Method's name to execute on the Facade's API|
|args|object[]|Arguments for the method (must be serializables for Json to pass into JS)|

##### Returns

IUniverJsInterop: This, for linking

---------

### ResolveAsync

```csharp
Task ResolveAsync()
```

Resolve the queue

##### Returns

Task: Awaitable task for resolving the action queue

---------

### ResolveAsync<T>

```csharp
Task<T> ResolveAsync<T>()
```

Resolve the queue

##### Returns

`Task<T>`: Awaitable task returning a typed value

---------

### ResolveActionAsync<T>

```csharp
Task<T> ResolveActionAsync<T>(string name, params object[] args)
```

Resolve a function in the JavaScript module

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|name|string|Name of the function|
|args|object[]|Arguments for that method|

##### Returns

`Task<T>`: The type desired for the function

---------

### ResolveActionAsync

```csharp
Task ResolveActionAsync(string name, params object[] args)
```

Resolve a function in the JavaScript module

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|name|string|Name of the function|
|args|object[]|Arguments for that method|

##### Returns

Task: Awaitable task for executing a JS function

---------

### GetUniverLinks

```csharp
string[] GetUniverLinks()
```

Gets all scripts components for Univer

##### Returns

string[]: An array of each Univer library to import