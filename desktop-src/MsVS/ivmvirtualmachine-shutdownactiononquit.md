---
title: IVMVirtualMachine ShutdownActionOnQuit property
description: The ShutdownActionOnQuit property contains how to shut down this virtual machine (VM) if it is running when Virtual Server is quit.
ms.assetid: bb876358-52d1-4234-817a-f7e237e780f7
keywords:
- ShutdownActionOnQuit property Virtual Server
- ShutdownActionOnQuit property Virtual Server , IVMVirtualMachine interface
- IVMVirtualMachine interface Virtual Server , ShutdownActionOnQuit property
- ShutdownActionOnQuit property Virtual Server , VMVirtualMachine interface
- VMVirtualMachine interface Virtual Server , ShutdownActionOnQuit property
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ShutdownActionOnQuit
- IVMVirtualMachine.get_ShutdownActionOnQuit
- IVMVirtualMachine.put_ShutdownActionOnQuit
- VMVirtualMachine.ShutdownActionOnQuit
api_location:
- VsComInterfaces.h
api_type:
- COM
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# IVMVirtualMachine::ShutdownActionOnQuit property

The **ShutdownActionOnQuit** property contains how to shut down this virtual machine (VM) if it is running when Virtual Server is quit.

This property is read/write.

## Syntax


```C++
HRESULT put_ShutdownActionOnQuit(
  [in]  VMShutdownAction shutdownAction
);

HRESULT get_ShutdownActionOnQuit(
  [out] VMShutdownAction *shutdownAction
);
```

<span codelanguage="VisualBasic"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>VMVirtualMachine.ShutdownActionOnQuit( _
  ByRef shutdownAction, _
  ByVal shutdownAction _
)</code></pre></td>
</tr>
</tbody>
</table>



## Property value

Contains a flag which specifies how to shut down this VM if it is running when Virtual Server is quit.

This property value is read/write.

## Error codes



| Name                                                                                          | Meaning                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>S\_OK</dt> </dl>              | The operation was successful.<br/>          |
| <dl> <dt>E\_POINTER</dt> </dl>         | *shutdownAction* is **NULL**.<br/>          |
| <dl> <dt>E\_POINTER</dt> </dl>         | *shutdownAction* is not a valid value.<br/> |
| <dl> <dt>VM\_E\_VM\_UNKNOWN</dt> </dl> | The configuration is unknown.<br/>          |
| <dl> <dt>DISP\_E\_EXCEPTION</dt> </dl> | An unexpected error has occurred.<br/>      |



## Remarks

By default, running VMs are saved when Virtual Server is quit. The shutdown action [**vmShutdownAction\_Save**](vmshutdownaction.md) will save the VM's state. The **vmShutdownAction\_TurnOff** action will turn off the VM. The **vmShutdownAction\_Shutdown** action will shut down the guest operating system if the Virtual Server Additions are available and will fall back onto saving the VM otherwise.

## Examples

The following example displays the **ShutdownActionOnQuit** property value of a [**VMVirtualMachine**](ivmvirtualmachine.md) object.


```VB
Set objVS = CreateObject("VirtualServer.Application")
Set objVM = objVS.FindVirtualMachine("Windows Server 2003")

WScript.Echo "VM Name: " & objVM.Name
WScript.Echo "Shutdown action on quit: " & objVM.ShutdownActionOnQuit
```



## Requirements



|                     |                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------|
| Product<br/>  | Microsoft Virtual Server 2005 onWindows Server 2003<br/>                                    |
| Download<br/> | Microsoft Virtual Server 2005 R2 SP1 Update onWindows Server 2008orWindows Server 2003<br/> |
| Header<br/>   | <dl> <dt>VsComInterfaces.h</dt> </dl>      |



## See also

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> <dt>

[**VMShutdownAction**](vmshutdownaction.md)
</dt> </dl>

 

 




