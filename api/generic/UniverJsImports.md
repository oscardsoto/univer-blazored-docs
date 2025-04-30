---
layout: page
title: UniverJsImports
parent: Generic
nav_order: 5
---

# {{ page.title }}

Module to extract scripts and import them on a page.

```csharp
public class UniverJsImports : IAsyncDisposable
```

## Remarks

This module is used to import all libraries from Univer's NPM to the HTML document, depending of wich component the user will execute inside the blazor page.

If the Spreadsheet component is imported in the page, all presets from Univer will be imported as well.

(See [installation and basic usage](https://docs.univer.ai/en-US/guides/sheets/getting-started/installation) for more information)

## Constructor

### UniverJsImports

```csharp
public UniverJsImports(IJSRuntime jsRuntime)
```

Initializes the module to extract scripts and import them on a page.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|jsRuntime|IJSRuntime|JavaScript Runtime used to load the module|

## Methods

### ImportLibrary

```csharp
public async Task<bool> ImportLibrary(string uri, bool isScript)
```

Imports a script or a resource for use in the page that contains Univer's component.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|uri|string|URI of the script or resource to import|
|isScript|bool|Whether the resource is a script or not|

##### Returns

`Task<bool>`: A task that returns true if the script was successfully imported

---

### DisposeAsync

```csharp
public async ValueTask DisposeAsync()
```

Disposes the JavaScript module if it has been created.

##### Returns

ValueTask: Awaitable task to release the JS resources