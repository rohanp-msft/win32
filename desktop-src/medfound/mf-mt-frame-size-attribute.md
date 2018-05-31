---
Description: Width and height of a video frame, in pixels.
ms.assetid: 9f10a972-406f-47ef-b71c-86ed771c9a9a
title: MF\_MT\_FRAME\_SIZE attribute
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# MF\_MT\_FRAME\_SIZE attribute

Width and height of a video frame, in pixels.

## Data type

**UINT64**

## Remarks

The upper 32 bits contain the width and the lower 32 bits contain the height.

To set this attribute, use the [**MFSetAttributeSize**](/windows/win32/mfapi/nf-mfapi-mfsetattributesize?branch=master) function. To get this attribute, use the [**MFGetAttributeSize**](/windows/win32/mfapi/nf-mfapi-mfgetattributesize?branch=master) function.

The GUID constant for this attribute is exported from mfuuid.lib.

## Examples


```
// Helper function to set the frame size on a video media type.
inline HRESULT SetFrameSize(IMFMediaType *pType, UINT32 width, UINT32 height)
{
    return MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
}

// Helper function to get the frame size from a video media type.
inline HRESULT GetFrameSize(IMFMediaType *pType, UINT32 *pWidth, UINT32 *pHeight)
{
    return MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, pWidth, pHeight);
}
```



## Requirements



|                                     |                                                                                    |
|-------------------------------------|------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps \| UWP apps\]<br/>                              |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps \| UWP apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## See also

<dl> <dt>

[Alphabetical List of Media Foundation Attributes](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFMediaType**](/windows/win32/mfobjects/nn-mfobjects-imfmediatype?branch=master)
</dt> <dt>

[Media Type Attributes](media-type-attributes.md)
</dt> </dl>

 

 



