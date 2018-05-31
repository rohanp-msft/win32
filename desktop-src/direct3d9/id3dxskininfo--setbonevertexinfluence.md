---
Description: Sets an influence value of a bone on a single vertex.
ms.assetid: 9283866f-3dfe-467d-a74f-77e89c2778c4
title: ID3DXSkinInfoSetBoneVertexInfluence method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# ID3DXSkinInfo::SetBoneVertexInfluence method

Sets an influence value of a bone on a single vertex.

## Syntax


```C++
HRESULT SetBoneVertexInfluence(
  [in] DWORD boneNum,
  [in] DWORD influenceNum,
  [in] FLOAT weight
);
```



## Parameters

<dl> <dt>

*boneNum* \[in\]
</dt> <dd>

Type: **[**DWORD**](winprog.windows_data_types)**

Index of the bone. Must be between 0 and the number of bones.

</dd> <dt>

*influenceNum* \[in\]
</dt> <dd>

Type: **[**DWORD**](winprog.windows_data_types)**

Index of the influence array of the specified bone.

</dd> <dt>

*weight* \[in\]
</dt> <dd>

Type: **[**FLOAT**](winprog.windows_data_types)**

Blend factor of the specified bone influence.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

If the method succeeds, the return value is S\_OK. If the method fails, the return value can be D3DERR\_INVALIDCALL.

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneVertexInfluence**](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneInfluence**](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 



