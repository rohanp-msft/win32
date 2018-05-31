---
title: DBCOMMANDOP
description: DBCOMMANDOP
ms.assetid: 564e287b-ab3c-484e-8818-1d24ba5246ce
keywords:
- DBCOMMANDOP
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# DBCOMMANDOP

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](https://msdn.microsoft.com/library/windows/desktop/aa965362) for client side search and [Microsoft Search Server Express]( http://go.microsoft.com/fwlink/p/?linkid=258445) for server side search.

 

The **DBCOMMANDOP** type specifies the operation for a command node in the OLE DB command tree.

``` syntax
typedef WORD DBCOMMANDOP;
```

### Remarks

In each [**DBCOMMANDTREE**](dbcommandtree.md) structure representing a node in the command tree, **DBCOMMANDOP** takes on the appropriate DBOP\_\* operation value from the [**DBCOMMANDOPENUM**](/windows/previous-versions/cmdtree/ne-cmdtree-dbcommandopenum?branch=master) enumeration, as described in the [Data Manipulation Operators](data-manipulation-operators.md) and Data Definition Operators section of this reference.

## Related topics

<dl> <dt>

[**DBCOMMANDOPENUM**](/windows/previous-versions/cmdtree/ne-cmdtree-dbcommandopenum?branch=master)
</dt> <dt>

[**DBCOMMANDTREE**](dbcommandtree.md)
</dt> </dl>

 

 



