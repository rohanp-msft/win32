---
Description: The Skip method skips over a specified number of pins in the enumeration sequence. This method implements the IEnumPinsSkip method.
ms.assetid: d42f958c-f488-4730-ab84-fc4e4150b186
title: CEnumPins.Skip method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# CEnumPins.Skip method

The `Skip` method skips over a specified number of pins in the enumeration sequence. This method implements the [**IEnumPins::Skip**](/windows/win32/Strmif/nf-strmif-ienumpins-skip?branch=master) method.

## Syntax


```C++
HRESULT Skip(
   ULONG cPins
);
```



## Parameters

<dl> <dt>

*cPins* 
</dt> <dd>

Number of pins to skip.

</dd> </dl>

## Return value

Returns one of the **HRESULT** values shown in the following table.



| Return code                                                                                                | Description                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S\_FALSE**</dt> </dl>                    | Skipped past the end of the sequence.<br/>                                       |
| <dl> <dt>**S\_OK**</dt> </dl>                       | Success.<br/>                                                                    |
| <dl> <dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt> </dl> | The filter's state has changed and is now inconsistent with the enumerator.<br/> |



 

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CEnumPins Class**](cenumpins.md)
</dt> </dl>

 

 



