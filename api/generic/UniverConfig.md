---
layout: page  
title: UniverConfig
parent: Generic  
nav_order: 1
---

# UniverConfig

Configuration for Univer to initialize

```csharp
public class UniverConfig
```

## Remarks

Holds the necessary configuration to initialize the Univer component, including version, language, and initialization settings.

## Properties

| Name          | Type             | Description                                                             | Default                     |
|---------------|------------------|-------------------------------------------------------------------------|-----------------------------|
| Version     | string         | Univer's version.                                                       | "0.5.5"                  |
| Language    | [UniversLanguage]({% link api/generic/UniversLanguage.md %})| Univer's language.                                                      | UniversLanguage.ENGLISH  |
| InitialConfig | [UniverInit]({% link api/generic/UniverInit.md %})   | Configuration object that is sent to Univer to initialize the component.| new UniverInit()         |

---