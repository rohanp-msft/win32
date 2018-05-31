---
title: WSMan.Error property
description: Gets additional error information, in an XML stream, for the preceding call to a WSMan method if Windows Remote Management service was unable to create a Session object, a ConnectionOptions object, or a ResourceLocator object.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.prod: windows-server-dev
ms.technology: windows-remote-management
ms.tgt_platform: multiple
keywords:
- Error property Windows Remote Management
- Error property Windows Remote Management , WSMan object
- WSMan object Windows Remote Management , Error property
topic_type:
- apiref
api_name:
- WSMan.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# WSMan.Error property

Gets additional error information, in an XML stream, for the preceding call to a [**WSMan**](wsman.md) method if Windows Remote Management service was unable to create a [**Session**](session.md) object, a [**ConnectionOptions**](connectionoptions.md) object, or a [**ResourceLocator**](resourcelocator.md) object.

This property is read-only.

## Syntax


```VB
WSMan.Error As BSTR
```



## Property value

The XML representation of the error information.

## Requirements



|                                     |                                                                                          |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista<br/>                                                                 |
| Minimum supported server<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Library<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## See also

<dl> <dt>

[**WSMan**](wsman.md)
</dt> </dl>

 

 




