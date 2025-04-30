---
layout: page
title: URichTextValue
parent: Rich Text
grand_parent: Data
nav_order: 1
---

# {{ page.title }}

Fragment of IDocumentBody, from Univer, to create and get all Rich Texts [See doc](https://github.com/dream-num/univer/blob/dev/packages/core/src/types/interfaces/i-document-data.ts#L121)

```csharp
public struct URichTextValue
```

## Remarks

This struct represents a fragment of a rich text document body (IDocumentBody) from Univer. It contains the actual text data and its associated styled segments, enabling rich text formatting operations.

## Properties

|Property|Type|Description|
|---|---|---|
|dataStream|string|Data in the rich text|
|textRuns|List<[UTextRun]({% link api/spreadsheets/data/rich-text/UTextRun.md %})>|Text configuration for each style|

## Constructors

```csharp
public URichTextValue()
```

Fragment of IDocumentBody, from Univer, to create and get all Rich Texts [See doc](https://github.com/dream-num/univer/blob/dev/packages/core/src/types/interfaces/i-document-data.ts#L121)

---------

```csharp
public URichTextValue(string richText)
```

Fragment of IDocumentBody, from Univer, to create and get all Rich Texts [See doc](https://github.com/dream-num/univer/blob/dev/packages/core/src/types/interfaces/i-document-data.ts#L121)

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|richText|string|Text inside the rich text|