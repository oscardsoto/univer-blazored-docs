# Univer Blazored
A C# adaptation of Univer for creating and editing spreadsheets, documents, and slides on both web and server.

# What is Univer Blazored?
> "Univer is a full-stack framework for creating and editing spreadsheets, documents, and slides on both web and server." - Univer Team

Univer Blazored is a C# adaptation of the Univer framework, using its original CDN for integration into Blazor applications. This tool provides the necessary features to build Blazor projects based on spreadsheets, documents, and presentations efficiently and easily, preserving the core capabilities of the original framework without additional requirements.

# Pre-Requisite Knowledge
To use this library correctly, you must be familiarized with the Univer context first. Please read the framework documentation for a better understanding of Univer Blazored.

# Features
## For spreadsheets
- Values
- Formulas
- Styles
    - Cells
    - Text
- Merges
- Filters
- Conditional Format (beta)
- Comments
- Images
- Freeze columns and rows
- Rich text (on developement)
- Pivot Tables (on developement)
- Accesibility (on developement)
- And more!

## For Documents
> The Document component of Univer Blazored is still on developement. These features are not live at v1.0.
- Text
- Styles
- Formulas
- Images
- Comments

## License
Univer Blazored is distributed by an [Apache-2.0 license]()

## Basic Usage
Once the component is initialized, you can get access to the component's Agent and perform basic operations:

```csharp
var agent = Univer.Agent;
var sheets = await agent.GetSheetsInfo();
foreach (var sheet in sheets)
{
    await agent.SetActiveSheet(sheet.id);
    // Perform operations in the sheet
}
```

For more advance usage, visit the [get started]() section and for more detail of which operations the Agent can perform, visit [its documentation]() page depending on which component is used.