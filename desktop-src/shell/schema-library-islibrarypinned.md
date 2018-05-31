---
Description: The &lt;isLibraryPinned&gt; element specifies whether this library is pinned to the navigation pane in Windows Explorer. This element is optional and has no child elements and no attributes.
title: isLibraryPinned Element (Library Schema)
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# isLibraryPinned Element (Library Schema)

The &lt;isLibraryPinned&gt; element specifies whether this library is pinned to the navigation pane in Windows Explorer. This element is optional and has no child elements and no attributes.

## Syntax


```
<!-- isLibraryPinned -->
    <xs:element name="isLibraryPinned" type="xs:boolean" default="false" minOccurs="0"/>
```



## Element Information



| Parent Element                                                               | Child Elements |
|------------------------------------------------------------------------------|----------------|
| [libraryDescription Element (Library Schema)](schema-librarydescription.md) |                |



 

## Remarks

If true, the library is pinned to the Windows Explorer navigation pane.

## Related topics

<dl> <dt>

[libraryDescription Element (Library Schema)](schema-librarydescription.md)
</dt> <dt>

[searchConnectorDescription Element (Library Schema)](schema-library-searchconnectordescription.md)
</dt> </dl>

 

 


