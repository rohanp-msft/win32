---
Description: The photo metadata policy for the System.Photo.Contrast property.
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: System.Photo.Contrast Photo Metadata Policy
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# System.Photo.Contrast Photo Metadata Policy

The photo metadata policy for the [System.Photo.Contrast](http://msdn.microsoft.com/en-us/library/bb760407(VS.85).aspx) property.

### PKEY

PKEY\_Photo\_Contrast

### Containers

JPEG, TIFF

### Read-Only

No

### Output PROPVARIANT Type

VT\_UI4

### Input Type

UShort

### Conflict Resolution Policy

Values from different schemas are reconciled.

### JPEG Policy

### Read Paths



| Order | Path                          | Disk Format |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41992} | ushort      |
| 2     | /xmp/exif:Contrast            | unicode     |



 

### Write Paths



| Order | Path                          | Disk Format |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41992} | ushort      |
| 2     | /xmp/exif:Contrast            | unicode     |



 

### Remove Paths



| Order | Path                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=41992} |
| 2     | /xmp/exif:contrast            |



 

### TIFF Policies

### Read Paths



| Order | Path                     | Disk Format |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=41992} | ushort      |
| 2     | /ifd/xmp/exif:Contrast   | unicode     |



 

### Write Paths



| Order | Path                     | Disk Format |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=41992} | ushort      |
| 2     | /ifd/xmp/exif:Contrast   | unicode     |



 

### Remove Paths



| Order | Path                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort=41992} |
| 2     | /ifd/xmp/exif:contrast   |



 

## Remarks

## Related topics

<dl> <dt>

[System.Photo.Contrast](http://msdn.microsoft.com/en-us/library/bb760407(VS.85).aspx)
</dt> </dl>

 

 


