---
title: TaskNamedValueCollection object
description: Scripting object that contains a collection of TaskNamedValuePair object name-value pairs.
ms.assetid: 440dc70b-02de-4974-ad2a-462491d12775
keywords:
- TaskNamedValueCollection object Task Scheduler
- TaskNamedValueCollection object Task Scheduler , described
topic_type:
- apiref
api_name:
- TaskNamedValueCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.date: 05/31/2018
ms.topic: interface
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# TaskNamedValueCollection object

Scripting object that contains a collection of [**TaskNamedValuePair**](tasknamedvaluepair.md) object name-value pairs.

## Members

The **TaskNamedValueCollection** object has these types of members:

-   [Methods](#methods)
-   [Properties](#properties)

### Methods

The **TaskNamedValueCollection** object has these methods.



| Method                                            | Description                                                        |
|:--------------------------------------------------|:-------------------------------------------------------------------|
| [**Clear**](tasknamedvaluecollection-clear.md)   | Clears the entire collection of name-value pairs.<br/>       |
| [**Create**](tasknamedvaluecollection-create.md) | Creates a name-value pair in the collection.<br/>            |
| [**Remove**](tasknamedvaluecollection-remove.md) | Removes a selected name-value pair from the collection.<br/> |



 

### Properties

The **TaskNamedValueCollection** object has these properties.



| Property                                                   | Description                                                        |
|:-----------------------------------------------------------|:-------------------------------------------------------------------|
| [**Count**](tasknamedvaluecollection-count.md)<br/> | Gets the number of name-value pairs in the collection.<br/>  |
| [**Item**](tasknamedvaluecollection-item.md)<br/>   | Gets the specified name-value pair from the collection.<br/> |



 

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                          |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                                    |
| Type library<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## See also

<dl> <dt>

[**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md)
</dt> <dt>

[**EmailAction.HeaderFields**](emailaction-headerfields.md)
</dt> </dl>

 

 




