---
title: Configuration
layout: home
nav_order: 4
permalink: /config/
---
# Configuration

Univer Blazored needs 3 aspects to configure before initialize:
 
- [Language](#language)
- [Version](#version)
- [Initial Configuration](#initial-configuration), wich is an object that indicates wich Preset of Univer will be instanced

Each component has it's own Scoped running in the project, so each one has to be initialized on the builder services:

```csharp
...
builder.Services.AddRazorComponents()
    .AddInteractiveServerComponents();

builder.Services.AddUniverSpreadsheets(config => {
    // Language
    // Version
    // Init
});
builder.Services.AddUniverDocuments(config => {
    // Language
    // Version
    // Init
});
builder.Services.AddUniverPresentations(config => {
    // Language
    // Version
    // Init
});
...
```

## Language

You can choose the language of the Univer instance with [UniversLanguage]({% link api/generic/UniversLanguage.md %}).
```csharp
builder.Services.AddUniverSpreadsheets(config => {
    config.Language = UniverBlazored.Generic.UniversLanguage.ENGLISH;
    ...
    ...
});
```

## Version

You can choose the version of Univer by string:

{: .important }
> Univer Blazored works from version 0.6.7 or higher from Univer.
>
> Malfunctions can be present if the version is lower

```csharp
builder.Services.AddUniverSpreadsheets(config => {
    ...
    config.Version = "0.6.9";
    ...
});
```

## Initial Configuration

You can choose which properties of Univer will be executed before the application start by [UniverInit]({% link api/generic/UniverInit.md %}) object:

```csharp
builder.Services.AddUniverSpreadsheets(config => {
    ...
    ...
    config.InitialConfig = new UniverBlazored.Generic.UniverInit()
    {
        hasConditionalFormatting    = true,
        hasCrosshair                = true,
        hasDrawing                  = true, // Also used in Documents
        hasFilter                   = true,
        hasThreadComment            = true, // Also used in Documents
        hasShort                    = true,
        hasHyperLink                = true, // Also used in Documents
        hasDataValidation           = true,
        hasWatermark                = false, // Also used in Documents
        newSheetName                = "UniverSheet"
    };
});
```