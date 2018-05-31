---
title: Retrieving a User SDO
description: Retrieving a User SDO
audience: developer
author: REDMOND\\markl
manager: REDMOND\\mbaldwin
ms.assetid: 440628f8-081b-4e7f-bdb2-760ff9bd0d77
ms.prod: windows-server-dev
ms.technology: network-policy-and-access-services
ms.tgt_platform: multiple
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# Retrieving a User SDO

The following code retrieves a Server Data Object (SDO) for the Administrator.


```C++
   HRESULT  hr;
   _bstr_t bstrUserName = L"Administrator";
   CComPtr<IUnknown> pUserUnknown;

   hr = pSdoMachine->GetUserSDO(
      DATA_STORE_LOCAL,
      bstrUserName,
      (IUnknown**) &amp;pUserUnknown
   );
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pUserSDO;
   hr = pUserUnknown->QueryInterface(
      __uuidof(ISdo),
      (void**) &amp;pUserSDO
   );
   if (FAILED(hr))
   {
      return hr;
   }
```



## Related topics

<dl> <dt>

[Attaching to an SDO-Enabled Computer](https://msdn.microsoft.com/library/bb960609)
</dt> <dt>

[**ISdo**](https://msdn.microsoft.com/library/bb960639)
</dt> <dt>

[**ISdoMachine**](https://msdn.microsoft.com/library/bb960655)
</dt> <dt>

[**ISdoMachine::GetUserSDO**](https://msdn.microsoft.com/library/bb960662)
</dt> <dt>

[**SysAllocString**](9e0437a2-9b4a-4576-88b0-5cb9d08ca29b)
</dt> <dt>

[**SysFreeString**](8f230ee3-5f6e-4cb9-a910-9c90b754dcd3)
</dt> </dl>

 

 



