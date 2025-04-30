---
layout: page
title: UniverUserType
parent: Data
grand_parent: Generic
nav_order: 5
---

# {{ page.title }}

User type, used in the UserManager

```csharp
public enum UniverUserType
```

## Fields

| Name         | Value | Description             |
|--------------|-------|-------------------------|
| UNRECOGNIZED | 0     | User not recognized.    |
| Owner        | 1     | User Owner.             |
| Editor       | 2     | Only edit.              |
| Reader       | 3     | Only read.              |

## Remarks
This enum defines user roles within the `UserManager` context of Univer. It specifies whether a user has ownership rights, edit access, read-only access, or is unrecognized.