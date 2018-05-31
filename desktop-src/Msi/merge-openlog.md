---
Description: The OpenLog method of the Merge object opens a log file that receives progress and error messages. If the log file already exists, the installer appends new messages. If the log file does not exist, the installer creates a log file.
ms.assetid: b34e7f28-2cf3-4cc7-9a39-e1da6fb8c788
title: Merge.OpenLog method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Merge.OpenLog method

The **OpenLog** method of the [**Merge**](merge-object.md) object opens a log file that receives progress and error messages. If the log file already exists, the installer appends new messages. If the log file does not exist, the installer creates a log file.

## Syntax


```JScript
Merge.OpenLog(
  Filename
)
```



## Parameters

<dl> <dt>

*Filename* 
</dt> <dd>

Fully qualified file name pointing to a file to open or create.

</dd> </dl>

## Return value

This method does not return a value.

## Remarks

Clients may send their own messages to this log file through the [**Log**](merge-log.md) method.

### C++

See [**OpenLog**](/windows/win32/Mergemod/?branch=master) function.

## Requirements



|                    |                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1.0 or later<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 



