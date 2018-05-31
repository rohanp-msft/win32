---
Description: The GetAvailable method retrieves the range of times in which seeking is efficient. This method implements the IMediaSeekingGetAvailable method.
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: CPosPassThru.GetAvailable method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# CPosPassThru.GetAvailable method

The `GetAvailable` method retrieves the range of times in which seeking is efficient. This method implements the [**IMediaSeeking::GetAvailable**](/windows/win32/Strmif/nf-strmif-imediaseeking-getavailable?branch=master) method.

## Syntax


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## Parameters

<dl> <dt>

*pEarliest* 
</dt> <dd>

Pointer to a variable that receives the earliest time for efficient seeking.

</dd> <dt>

*pLatest* 
</dt> <dd>

Pointer to a variable that receives the latest time for efficient seeking.

</dd> </dl>

## Return value

Returns the **HRESULT** value from the connected pin.

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CPosPassThru Class**](cpospassthru.md)
</dt> </dl>

 

 



