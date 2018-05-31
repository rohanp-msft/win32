---
Description: Proxy function for the GetDataPointer method.
ms.assetid: 7256d6eb-cb7c-4067-8382-511d64da6825
title: IWICBitmapLock\_GetDataPointer\_STA\_Proxy function
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# IWICBitmapLock\_GetDataPointer\_STA\_Proxy function

Proxy function for the [**GetDataPointer**](/windows/win32/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer?branch=master) method.

## Syntax


```C++
HRESULT IWICBitmapLock_GetDataPointer_STA_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbBufferSize,
  _Out_ BYTE           **ppbData
);
```



## Parameters

<dl> <dt>

*THIS\_PTR* \[in\]
</dt> <dd>

Type: **[**IWICBitmapLock**](/windows/win32/Wincodec/nn-wincodec-iwicbitmaplock?branch=master)\***

Pointer to this [**IWICBitmapLock**](/windows/win32/Wincodec/nn-wincodec-iwicbitmaplock?branch=master) object.

</dd> <dt>

*pcbBufferSize* \[out\]
</dt> <dd>

Type: **UINT\***

A pointer that receives the size of the buffer.

</dd> <dt>

*ppbData* \[out\]
</dt> <dd>

Type: **BYTE\*\***

A pointer that receives a pointer to the top left pixel in the locked rectangle.

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



 

 



