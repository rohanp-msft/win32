---
title: UsnReadMinSize
description: UsnReadMinSize
ms.assetid: 406308f5-d87d-4935-8ee0-04ec995975ac
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# UsnReadMinSize

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](https://msdn.microsoft.com/library/windows/desktop/aa965362) for client side search and [Microsoft Search Server Express]( http://go.microsoft.com/fwlink/p/?linkid=258445) for server side search.

 

The **UsnReadMinSize** entry is the minimum size that the USN journal must attain before processing of change notifications can proceed.

### Summary



|          |                |
|----------|----------------|
| Type:    | **REG\_DWORD** |
| Units:   | Bytes          |
| Default: | 4096           |
| Range:   | 1 - 524288     |



 

### Remarks

The processing of change notifications proceeds when either the size of the USN journal reaches the value of the **UsnReadMinSize** entry or an interval of time equal to the value of the [**UsnReadTimeout**](usnreadtimeout.md) entry has passed (and there are entries in the USN journal).

## Related topics

<dl> <dt>

[Catalog, Property, and Scope Registry Entries](catalog--property--and-scope-registry-entries.md)
</dt> <dt>

[Main Registry Entries](main-registry-entries.md)
</dt> <dt>

[**UsnReadTimeout**](usnreadtimeout.md)
</dt> </dl>

 

 



