---
title: REASSIGN\_BLOCKS structure
description: The REASSIGN\_BLOCKS structure is used in conjunction with the IOCTL\_DISK\_REASSIGN\_BLOCKS request to instruct a disk device to reassign the block numbers of the indicated bad blocks to good blocks.
ms.assetid: d79f8e47-87c5-4203-b9d7-722d9be4e848
keywords:
- REASSIGN_BLOCKS structure Storage Devices
- PREASSIGN_BLOCKS structure pointer Storage Devices
topic_type:
- apiref
api_name:
- REASSIGN_BLOCKS
api_location:
- ntdddisk.h
api_type:
- HeaderDef
ms.date: 05/31/2018
ms.topic: structure
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# REASSIGN\_BLOCKS structure

The **REASSIGN\_BLOCKS** structure is used in conjunction with the [**IOCTL\_DISK\_REASSIGN\_BLOCKS**](ioctl-disk-reassign-blocks.md) request to instruct a disk device to reassign the block numbers of the indicated bad blocks to good blocks.

## Syntax


```C++
typedef struct _REASSIGN_BLOCKS {
  USHORT Reserved;
  USHORT Count;
  ULONG  BlockNumber[1];
} REASSIGN_BLOCKS, *PREASSIGN_BLOCKS;
```



## Members

<dl> <dt>

**Reserved**
</dt> <dd>

Reserved for system use.

</dd> <dt>

**Count**
</dt> <dd>

Contains the number of blocks in the array pointed to by **BlockNumber** to reassign.

</dd> <dt>

**BlockNumber**
</dt> <dd>

Contains an array of block numbers corresponding to damaged blocks. These numbers will be reassigned to good blocks taken from the device's spare block pool.

</dd> </dl>

## Requirements



|                   |                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Ntdddisk.h (include Ntdddisk.h)</dt> </dl> |



## See also

<dl> <dt>

[**IOCTL\_DISK\_REASSIGN\_BLOCKS**](ioctl-disk-reassign-blocks.md)
</dt> </dl>

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bstorage\storage%5D:%20REASSIGN_BLOCKS%20structure%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")





