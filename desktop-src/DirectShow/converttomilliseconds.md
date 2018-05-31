---
Description: The ConvertToMilliseconds function converts a reference time to milliseconds.
ms.assetid: fae3baa4-9344-4197-b375-4abe2656e1b7
title: ConvertToMilliseconds function
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# ConvertToMilliseconds function

The `ConvertToMilliseconds` function converts a reference time to milliseconds.

## Syntax


```C++
LONGLONG ConvertToMilliseconds(
   const REFERENCE_TIME &amp;RT
);
```



## Parameters

<dl> <dt>

*RT* \[ref\]
</dt> <dd>

Reference time, in 100-nanosecond units.

</dd> </dl>

## Return value

Returns the reference time converted to milliseconds.

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Refclock.h (include Streams.h)</dt> </dl>                                                                                  |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CBaseReferenceClock Class**](cbasereferenceclock.md)
</dt> </dl>

 

 



