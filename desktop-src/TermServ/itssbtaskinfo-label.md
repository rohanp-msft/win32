---
title: ITsSbTaskInfo Label property
description: Retrieves the label that describes the purpose of the task.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 075de6a4-53b0-43b0-9bca-03bf312fff6e
ms.prod: windows-server-dev
ms.technology: remote-desktop-services
ms.tgt_platform: multiple
keywords:
- Label property Remote Desktop Services
- Label property Remote Desktop Services , ITsSbTaskInfo interface
- ITsSbTaskInfo interface Remote Desktop Services , Label property
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Label
- ITsSbTaskInfo.get_Label
api_location:
- Sbtsv.idl
api_type:
- COM
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# ITsSbTaskInfo::Label property

Retrieves the label that describes the purpose of the task.

This property is read-only.

## Syntax


```C++
HRESULT get_Label(
  [out, retval] BSTR *pLabel
);
```



## Property value

A pointer to a **BSTR** value that contains the label.

## Requirements



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                            |
| Minimum supported server<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## See also

<dl> <dt>

[**ITsSbTaskInfo**](/windows/win32/sbtsv/nn-sbtsv-itssbtaskinfo?branch=master)
</dt> </dl>

 

 




