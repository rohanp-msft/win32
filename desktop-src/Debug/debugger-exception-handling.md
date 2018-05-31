---
Description: The systems handling of user-mode exceptions provides support for sophisticated debuggers.
ms.assetid: c45a7dc6-e6b2-4fc4-9522-12d96893f4c7
title: Debugger Exception Handling
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Debugger Exception Handling

The system's handling of user-mode exceptions provides support for sophisticated debuggers. If the process in which an exception occurs is being debugged, the system generates a debug event. If the debugger is using the [**WaitForDebugEvent**](/windows/win32/WinBase/?branch=master) function, the debug event causes that function to return with a pointer to a [**DEBUG\_EVENT**](debug-event-str.md) structure. This structure contains the process and thread identifiers the debugger can use to access the thread's context record. The structure also contains an [**EXCEPTION\_DEBUG\_INFO**](exception-debug-info-str.md) structure that includes a copy of the exception record.

When the system is searching for an exception handler, it makes two attempts to notify a process's debugger. The first notification attempt provides the debugger with an opportunity to handle breakpoint or single-step exceptions. This is known as *first-chance notification*. The user can then issue debugger commands to manipulate the process's environment before any exception handlers are executed. The second attempt to notify the debugger occurs only if the system is unable to find a frame-based exception handler that handles the exception. This is known as *last-chance notification*. If the debugger does not handle the exception after the last-chance notification, the system terminates the process being debugged.

At each notification attempt, the debugger uses the [**ContinueDebugEvent**](/windows/win32/WinBase/?branch=master) function to return control to the system. Before returning control, the debugger can handle the exception and modify the thread state as appropriate, or it can choose not to handle the exception. Using **ContinueDebugEvent**, the debugger can indicate that it has handled the exception, in which case the machine state is restored and thread execution is continued at the point at which the exception occurred. The debugger can also indicate that it did not handle the exception, which causes the system to continue its search for an exception handler.

 

 


