---
Description: The get\_FramesDrawn method retrieves the m\_cFramesDrawn member variable, giving the number of frames drawn since streaming started.
ms.assetid: 486b5541-2952-47ce-944e-4efb8e5af9dd
title: CBaseVideoRenderer.get\_FramesDrawn method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# CBaseVideoRenderer.get\_FramesDrawn method

The `get_FramesDrawn` method retrieves the **m\_cFramesDrawn** member variable, giving the number of frames drawn since streaming started.

## Syntax


```C++
HRESULT get_FramesDrawn(
   int *pcFramesDrawn
);
```



## Parameters

<dl> <dt>

*pcFramesDrawn* 
</dt> <dd>

Pointer to the number of frames drawn.

</dd> </dl>

## Return value

Returns an **HRESULT** value.

## Remarks

This member function implements the [**IQualProp::get\_FramesDrawn**](/windows/win32/Amvideo/nf-amvideo-iqualprop-get_framesdrawn?branch=master) method.

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CBaseVideoRenderer Class**](cbasevideorenderer.md)
</dt> </dl>

 

 



