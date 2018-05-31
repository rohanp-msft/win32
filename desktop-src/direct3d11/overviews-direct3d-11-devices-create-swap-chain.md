---
title: How To Create a Swap Chain
description: This topic show how to create a swap chain that encapsulates two or more buffers that are used for rendering and display.
ms.assetid: 0e290b37-0807-42c7-9e50-fd2db6affb14
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# How To: Create a Swap Chain

This topic show how to create a swap chain that encapsulates two or more buffers that are used for rendering and display. They usually contain a front buffer that is presented to the display device and a back buffer that serves as the render target. After the immediate context is done rendering to the back buffer, the swap chain presents the back buffer by swapping the two buffers.

The swap chain defines several rendering characteristics including:

-   The size of the render area.
-   The display refresh rate.
-   The display mode.
-   The surface format.

Define the characteristics of the swap chain by filling in a [**DXGI\_SWAP\_CHAIN\_DESC**](https://msdn.microsoft.com/library/windows/desktop/bb173075) structure and initializing an [**IDXGISwapChain**](https://msdn.microsoft.com/library/windows/desktop/bb174569) interface. Initialize a swap chain by calling [**IDXGIFactory::CreateSwapChain**](https://msdn.microsoft.com/library/windows/desktop/bb174537) or [**D3D11CreateDeviceAndSwapChain**](/windows/win32/D3D11/nf-d3d11-d3d11createdeviceandswapchain?branch=master).

## Create a device and a swap chain

To initialize a device and swap chain, use one of the following two functions:

-   Use the [**D3D11CreateDeviceAndSwapChain**](/windows/win32/D3D11/nf-d3d11-d3d11createdeviceandswapchain?branch=master) function when you want to initialize the swap chain at the same time as device initialization. This usually is the easiest option.

-   Use the [**D3D11CreateDevice**](/windows/win32/D3D11/nf-d3d11-d3d11createdevice?branch=master) function when you have already created a swap chain using [**IDXGIFactory::CreateSwapChain**](https://msdn.microsoft.com/library/windows/desktop/bb174537).

## Related topics

<dl> <dt>

[Devices](overviews-direct3d-11-devices.md)
</dt> <dt>

[How to Use Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 



