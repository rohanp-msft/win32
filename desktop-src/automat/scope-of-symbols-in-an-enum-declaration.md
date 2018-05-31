---
title: Scope of Symbols in an enum Declaration
description: In MIDL, the scope of symbols in an enum is global with MIDL, as it is in C.
ms.assetid: 4748fe99-9a98-4677-b3aa-0065caa3278f
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Scope of Symbols in an enum Declaration

In MIDL, the scope of symbols in an enum is global with MIDL, as it is in C. In the following example, MIDL will generate a duplicate name error:


```C++
typedef struct { ... } a;
enum {a=1, b=2, c=3};
```



 

 



