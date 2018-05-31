---
Description: Generates an optimized vertex remapping for a triangle list. This function is commonly used after applying the face remapping generated by D3DXOptimizeFaces.
ms.assetid: a3b9cb68-204e-4e8f-a985-738d1cea1e29
title: D3DXOptimizeVertices function
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# D3DXOptimizeVertices function

Generates an optimized vertex remapping for a triangle list. This function is commonly used after applying the face remapping generated by [**D3DXOptimizeFaces**](d3dxoptimizefaces.md).

## Syntax


```C++
HRESULT D3DXOptimizeVertices(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pVertexRemap
);
```



## Parameters

<dl> <dt>

*pIndices* \[in\]
</dt> <dd>

Type: **[**LPCVOID**](winprog.windows_data_types)**

Pointer to triangle list indices to use for ordering vertices.

</dd> <dt>

*NumFaces* \[in\]
</dt> <dd>

Type: **[**UINT**](winprog.windows_data_types)**

Number of faces in the triangle list.

</dd> <dt>

*NumVertices* \[in\]
</dt> <dd>

Type: **[**UINT**](winprog.windows_data_types)**

Number of vertices referenced by the triangle list.

</dd> <dt>

*Indices32Bit* \[in\]
</dt> <dd>

Type: **[**BOOL**](winprog.windows_data_types)**

Flag indicating index type: **TRUE** if indices are 32-bit (more than 65535 vertices), **FALSE** if indices are 16-bit (65535 or fewer vertices).

</dd> <dt>

*pVertexRemap* \[in, out\]
</dt> <dd>

Type: **[**DWORD**](winprog.windows_data_types)\***

Pointer to a destination buffer that will contain the new index for each vertex. The value stored in *pVertexRemap* for a given element is the source vertex location in the new vertex ordering.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

If the function succeeds, the return value is D3D\_OK. If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.

## Remarks

By default, a mesh uses 16 bit indices when it is created unless the application specifies otherwise. To check whether an existing mesh uses 16-bit or 32-bit indices, call [**ID3DXBaseMesh::GetOptions**](id3dxbasemesh--getoptions.md) and check for the D3DXMESH\_32BIT flag.

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[Mesh Functions](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 



