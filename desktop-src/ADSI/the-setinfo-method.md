---
title: The SetInfo Method
description: The IADs SetInfo method saves the current values for the properties for this Active Directory object from the property cache to the underlying directory store. This is analogous to flushing a buffer out to disk.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\mbaldwin
ms.assetid: e4152b3d-3a59-4f69-9765-03cdf6286459
ms.prod: windows-server-dev
ms.technology: active-directory-domain-services
ms.tgt_platform: multiple
keywords:
- SetInfo ADSI ,using
- properties ADSI ,save the current values for properties
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# The SetInfo Method

The [**IADs::SetInfo**](/windows/win32/Iads/nf-iads-iads-setinfo?branch=master) method saves the current values for the properties for this Active Directory object from the property cache to the underlying directory store. This is analogous to flushing a buffer out to disk.

[**SetInfo**](/windows/win32/Iads/nf-iads-iads-setinfo?branch=master) updates objects that already exist in the directory, or create a new directory entry for newly created objects.

At the time of the [**SetInfo**](/windows/win32/Iads/nf-iads-iads-setinfo?branch=master) call, if any property cache values have been written with a [**PutEx**](/windows/win32/Iads/nf-iads-iads-putex?branch=master) control code, such as ADS\_PROPERTY\_UPDATE or ADS\_PROPERTY\_CLEAR, then the appropriate requests are passed on to the underlying directory service.

 

 



