---
Description: Save a texture to a file.
ms.assetid: c1718903-039a-4132-b128-82e03078ef62
title: D3DX10SaveTextureToFile function
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# D3DX10SaveTextureToFile function

Save a texture to a file.

## Syntax


```C++
HRESULT D3DX10SaveTextureToFile(
  _In_ ID3D10Resource           *pSrcTexture,
  _In_ D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## Parameters

<dl> <dt>

*pSrcTexture* \[in\]
</dt> <dd>

Type: **[**ID3D10Resource**](/windows/win32/D3D10/nn-d3d10-id3d10resource?branch=master)\***

Pointer to the texture to be saved. See [**ID3D10Resource Interface**](/windows/win32/D3D10/nn-d3d10-id3d10resource?branch=master).

</dd> <dt>

*DestFormat* \[in\]
</dt> <dd>

Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**

The format the texture will be saved as (see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)). D3DX10\_IFF\_DDS is the preferred format since it is the only option that supports all the formats in [**DXGI\_FORMAT**](direct3ddxgi.dxgi_format).

</dd> <dt>

*pDestFile* \[in\]
</dt> <dd>

Type: **[**LPCTSTR**](winprog.windows_data_types)**

Name of the destination output file where the texture will be saved. If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR. Otherwise, the data type resolves to LPCSTR.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md); use the return value to see if the *DestFormat* is supported.

## Remarks

**D3DX10SaveTextureToFile** writes out the extra [**DDS\_HEADER\_DXT10**](direct3ddds.dds_header_dxt10) structure for the input texture only if necessary (for example, because the input texture is in standard RGB (sRGB) format). If **D3DX10SaveTextureToFile** writes out the **DDS\_HEADER\_DXT10** structure, it sets the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](direct3ddds.dds_pixelformat) structure for the texture to **DX10** to indicate the prescense of the **DDS\_HEADER\_DXT10** extended header.

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## See also

<dl> <dt>

[Texture Functions in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[General Purpose Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 



