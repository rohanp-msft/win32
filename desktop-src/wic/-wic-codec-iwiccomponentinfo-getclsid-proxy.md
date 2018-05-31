---
Description: Proxy function for the GetCLSID method.
ms.assetid: c6a8d752-590f-43d6-bac8-72b5bd259ad0
title: IWICComponentInfo\_GetCLSID\_Proxy function
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# IWICComponentInfo\_GetCLSID\_Proxy function

Proxy function for the [**GetCLSID**](/windows/win32/Wincodec/nf-wincodec-iwiccomponentinfo-getclsid?branch=master) method.

## Syntax


```C++
HRESULT IWICComponentInfo_GetCLSID_Proxy(
  _In_  IWICComponentInfo *THIS_PTR,
  _Out_ CLSID             *pclsid
);
```



## Parameters

<dl> <dt>

*THIS\_PTR* \[in\]
</dt> <dd>

Type: **[**IWICComponentInfo**](/windows/win32/Wincodec/nn-wincodec-iwiccomponentinfo?branch=master)\***

Pointer to this [**IWICComponentInfo**](/windows/win32/Wincodec/nn-wincodec-iwiccomponentinfo?branch=master) object.

</dd> <dt>

*pclsid* \[out\]
</dt> <dd>

Type: **CLSID\***

A pointer that receives the component's CLSID.

</dd> </dl>

## Return value

Type: **HRESULT**

If this function succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Remarks

## Requirements



|                                     |                                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows XP with SP2, Windows Vista \[desktop apps only\]<br/>                                                                                              |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 



