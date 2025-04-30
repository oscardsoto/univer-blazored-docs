---
title: Installation
layout: home
nav_order: 3
permalink: /install/
---

# Installation

1. Install the package via NuGet:
    ```console
    dotnet add package UniverBlazored --version 1.0
    ```

    To install the Spreadsheet Converter extension, install it also via NuGet:
    ```console
    dotnet add package UniverBlazored.SpreadsheetConverter --version 1.0
    ```

    {: .important}
    Consider in your project that UniverBlazored.SpreadsheetConverter uses ClosedXML v0.104.2

2. Implement the namespaces and the services in your project:
    ```csharp
    ...
    using UniverBlazored.Spreadsheets;


    ...
    builder.Services.AddUniverSpreadsheets(config => {
        config.Language = UniverBlazored.Generic.UniversLanguage.ENGLISH;
        config.Version = "0.6.9";
        config.InitialConfig = new UniverBlazored.Generic.UniverInit()
        {
            hasConditionalFormatting = true,
            hasCrosshair = true,
            hasThreadComment = true,
            newSheetName = "UniverSheet"
        };
    });
    ...
    ```

    For more information about configuration, visit the [configuration]({% link config.md %}) options.

    For Spreadsheet Converter service:

    ```csharp
    ...
    using UniverBlazored.SpreadsheetConverter;


    ...
    builder.Services.AddUniverSpreadsheetsConverter(config => {
        config.MaxCellsReaded = 1000;
    });
    ...
    ```

3. Implement the namespace and the desired component in the page.
    Make sure to implement the correct render mode in the page, which is `InteractiveServer`.

    ```csharp
    @page "/your-page"
    @using UniverBlazored.Spreadsheets.Components;
    ...
    @rendermode InteractiveServer

    // Your code here
    <UniverSpreadsheetControl CssClass="univer-custom" @ref="Univer"></UniverSpreadsheetControl>
    // ...

    @code{
        UniverSpreadsheetControl Univer = new();

        protectec override async Task OnAfterRenderAsync(bool firstRender)
        {
            // DO something with Univer..
        }
    }
    ```

    {: .important}
    > Make sure to do all Agent operations after the page renders. Univer Blazored executes after the page renders to correctly apply all presets.


## Basic Usage

Once the component is initialized, you can get access to the component's Agent:

```csharp
var agent = Univer.Agent;
var sheets = await agent.GetSheetsInfo();
foreach (var sheet in sheets)
{
    await agent.SetActiveSheet(sheet.id);
    // Perform operations in the sheet
}
```

For more advance usage, visit the [get started]({% link get-started.md %}) section, and for more detail of which operations the Agent can perform, visit its documentation page, depending of which component is used.