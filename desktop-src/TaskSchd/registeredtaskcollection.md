---
title: RegisteredTaskCollection object
description: Scripting object that contains all the tasks that are registered.
ms.assetid: 97403825-5762-477c-9695-3775bb5bc9e4
keywords:
- RegisteredTaskCollection object Task Scheduler
- RegisteredTaskCollection object Task Scheduler , described
topic_type:
- apiref
api_name:
- RegisteredTaskCollection
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

# RegisteredTaskCollection object

Scripting object that contains all the tasks that are registered.

## Members

The **RegisteredTaskCollection** object has these types of members:

-   [Properties](#properties)

### Properties

The **RegisteredTaskCollection** object has these properties.



| Property                                                   | Access type          | Description                                                        |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [**Count**](registeredtaskcollection-count.md)<br/> | Read-only<br/> | Gets the number of registered tasks in the collection.<br/>  |
| [**Item**](registeredtaskcollection-item.md)<br/>   | Read-only<br/> | Gets the specified registered task from the collection.<br/> |



 

## Examples

For more information and example code for this scripting object, see [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                          |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                                    |
| Type library<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## See also

<dl> <dt>

[**TaskFolder.GetTasks**](taskfolder-gettasks.md)
</dt> </dl>

 

 




