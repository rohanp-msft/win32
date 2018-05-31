---
title: RB\_GETTOOLTIPS message
description: Retrieves the handle to any tooltip control associated with the rebar control.
ms.assetid: 87897b00-857f-4a8a-ae16-a48abf4c411d
keywords:
- RB_GETTOOLTIPS message Windows Controls
topic_type:
- apiref
api_name:
- RB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# RB\_GETTOOLTIPS message

Retrieves the handle to any tooltip control associated with the rebar control.

## Parameters

<dl> <dt>

*wParam* 
</dt> <dd>Must be zero.</dd> <dt>

*lParam* 
</dt> <dd>Must be zero.</dd> </dl>

## Return value

Returns an **HWND** value that is the handle to the tooltip control associated with the rebar control, or zero if no tooltip control is associated with the rebar control.

## Requirements



|                                     |                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                        |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 




