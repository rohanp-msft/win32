---
title: TSGRemoveConsentMsg method of the Win32\_TSGatewayServerSettings class
description: Removes the administrative message for the gateway server.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 626dc9ca-d6a1-48ab-84ec-cfccb8e720c2
ms.prod: windows-server-dev
ms.technology: remote-desktop-services
ms.tgt_platform: multiple
keywords:
- TSGRemoveConsentMsg method Remote Desktop Services
- TSGRemoveConsentMsg method Remote Desktop Services , Win32_TSGatewayServerSettings class
- Win32_TSGatewayServerSettings class Remote Desktop Services , TSGRemoveConsentMsg method
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGRemoveConsentMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# TSGRemoveConsentMsg method of the Win32\_TSGatewayServerSettings class

Removes the administrative message for the gateway server.

## Syntax


```mof
uint32 TSGRemoveConsentMsg();
```



## Parameters

This method has no parameters.

## Return value

Type: **uint32**

If the method succeeds, it returns zero. If the method is unsuccessful, it returns a nonzero value. For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).

## Remarks

You must be a member of the Administrators group to call this method.

Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes. MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK). They are installed on the server when you add the associated role by using the Server Manager. For more information about MOF files, see [Managed Object Format (MOF)](https://msdn.microsoft.com/library/aa823192).

## Requirements



|                                     |                                                                                          |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                                |
| Minimum supported server<br/> | Windows Server 2008 R2<br/>                                                        |
| Namespace<br/>                | Root\\CIMv2\\TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## See also

<dl> <dt>

[**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 




