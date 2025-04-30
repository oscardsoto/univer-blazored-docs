---
layout: page  
title: UniverUserManager
parent: Services  
grand_parent: Generic
nav_order: 1  
---

# {{ page.title }}

User Manager from Univer

```csharp
public class UniverUserManager
```

## Remarks

Handles user-related operations within the Univer app using JS Interop. Includes methods to get, list, add, delete, and set current users.

## Constructor

```csharp
public UniverUserManager(IUniverJsInterop service)
```

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|service|[IUniverJsInterop]({% link api/generic/IUniverJsInterop.md %})|JS Interop service for Univer|

## Methods

### GetCurrentUser

```csharp
public async Task<UniverUser> GetCurrentUser()
```

Returns the current user using the Univer App.

##### Returns

Task<[UniverUser]({% link api/generic/data/UniverUser.md %})>: The current user object.

---

### ListAllUsers

```csharp
public async Task<List<UniverUser>> ListAllUsers()
```

Returns a list with all users in the Univer App.

##### Returns

Task< List<[UniverUser]({% link api/generic/data/UniverUser.md %})> >: List of all users.

---

### GetUser

```csharp
public async Task<UniverUser> GetUser(string idUser)
```

Returns the user info in the manager.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|idUser|string|User Id|

##### Returns

Task<[UniverUser]({% link api/generic/data/UniverUser.md %})>: User object by ID.

---

### AddUser (single user)

```csharp
public void AddUser(UniverUser user, bool setCurrent = false)
```

Adds a user to the manager. Optionally sets as current.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|user|[UniverUser]({% link api/generic/data/UniverUser.md %})|New user to add|
|setCurrent|bool|True if the new user should be set as current|

---

### AddUser (multiple users)

```csharp
public void AddUser(params UniverUser[] users)
```

Adds a list of users to the manager.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|users|[UniverUser]({% link api/generic/data/UniverUser.md %})[]|Users to add|

---

### CleanList

```csharp
public async void CleanList()
```

Clears the user list in the manager.

---

### DeleteUser

```csharp
public async void DeleteUser(string idUser)
```

Deletes a user from the manager by ID.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|idUser|string|User Id in the list|

---

### SetCurrentUser

```csharp
public async void SetCurrentUser(UniverUser user)
```

Sets the current user for the component.

##### Parameters

|Parameter|Type|Description|
|---|---|---|
|user|[UniverUser]({% link api/generic/data/UniverUser.md %})|User object to set as current|

---