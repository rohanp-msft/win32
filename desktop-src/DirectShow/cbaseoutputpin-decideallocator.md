---
Description: The DecideAllocator method selects a memory allocator.
ms.assetid: cdc15b0e-ea1b-43aa-9267-95fa9db56ed5
title: CBaseOutputPin.DecideAllocator method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# CBaseOutputPin.DecideAllocator method

The `DecideAllocator` method selects a memory allocator.

## Syntax


```C++
virtual HRESULT DecideAllocator(
   IMemInputPin  *pPin,
   IMemAllocator **pAlloc
);
```



## Parameters

<dl> <dt>

*pPin* 
</dt> <dd>

Pointer to the input pin's [**IMemInputPin**](/windows/win32/Strmif/nn-strmif-imeminputpin?branch=master) interface.

</dd> <dt>

*pAlloc* 
</dt> <dd>

Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/win32/Strmif/nn-strmif-imemallocator?branch=master) interface.

</dd> </dl>

## Return value

Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.

## Remarks

This method is called at the end of the pin connection process. It performs the following steps:

1.  Calls the [**IMemInputPin::GetAllocatorRequirements**](/windows/win32/Strmif/nf-strmif-imeminputpin-getallocatorrequirements?branch=master) method to retrieve the input pin's buffer requirements, if any.
2.  Calls the [**IMemInputPin::GetAllocator**](/windows/win32/Strmif/nf-strmif-imeminputpin-getallocator?branch=master) method to request an allocator from the input pin. If the input pin does not provide an allocator, the output pin creates one by calling the [**CBaseOutputPin::InitAllocator**](cbaseoutputpin-initallocator.md) class method.
3.  Calls the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) class method, which sets the allocator properties. This is a pure virtual method; the derived class must implement it.
4.  Calls the [**IMemInputPin::NotifyAllocator**](/windows/win32/Strmif/nf-strmif-imeminputpin-notifyallocator?branch=master) method, which notifies the input pin of the allocator being used.

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CBaseOutputPin Class**](cbaseoutputpin.md)
</dt> </dl>

 

 



