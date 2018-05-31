---
Description: Sets a pointer to an optional callback function that computes the percentage of spherical harmonic (SH) computations completed and gives the caller the option of aborting the simulator.
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: ID3DXPRTEngineSetCallBack method
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# ID3DXPRTEngine::SetCallBack method

Sets a pointer to an optional callback function that computes the percentage of spherical harmonic (SH) computations completed and gives the caller the option of aborting the simulator.

## Syntax


```C++
HRESULT SetCallBack(
  [in] LPD3DXSHPRTSIMCB pCB,
  [in] FLOAT            Frequency,
  [in] LPVOID           lpUserContext
);
```



## Parameters

<dl> <dt>

*pCB* \[in\]
</dt> <dd>

Type: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Pointer to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function that computes the percentage of SH computations completed. The callback function must be implemented to return S\_OK to keep running the simulator. Any other value will abort the simulator.

</dd> <dt>

*Frequency* \[in\]
</dt> <dd>

Type: **[**FLOAT**](winprog.windows_data_types)**

Frequency of callback calls. The inverse of Frequency is approximately the number of times the callback function will be called.

</dd> <dt>

*lpUserContext* \[in\]
</dt> <dd>

Type: **[**LPVOID**](winprog.windows_data_types)**

Pointer to a user-defined value which is passed to the callback function. Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

The return value is S\_OK.

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 



