---
title: Get Started
layout: home
nav_order: 2
permalink: /get-started/
---
# {{ page.title }}

Each component of Univer Blazored has 3 main characteristics:

- The Agent
- The Js Interop
- and the User Manager

The Agent is the class that manage all capable actions that will be consulted to the FacadeAPI to Univer.

The Js Interop is the bridge between Blazor and Univer to execute all actions made by the Agent.

The User Manager is a scoped service that handle all data from a list of users using the component. Most of the time, this scoped will be used to label all comments from the sheet, so you must save the data used outside of the scoped.

## How does it work?

Once the component is initialized, you can access both the Agent and the User Manager form it. Both services use the Js Interop, because all need the bridge to communicate to Univer all actions performed, and get a response from it, if needed.

The Agent and the User Manager works this way: after a method is called, it queues the methods that are required with their respective parameters to the Js Interop.

![alt0](https://oscardsoto.github.io/univer-blazored-docs/assets/images/diagram0.png)

It also can call a method directly from the Js Interop if needed.

## Important notes

- All actions of the Agent must be called after the page renders. All actions will be called to Univer through the javascript Interop.
