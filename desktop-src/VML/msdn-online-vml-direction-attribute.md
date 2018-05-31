---
title: VML Direction Attribute
description: VML Direction Attribute
ms.assetid: bf6e0169-f0d4-4dfb-b59e-b5601049fd7a
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# VML Direction Attribute

This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9. Webpages and applications that rely on VML should be [migrated to SVG](http://go.microsoft.com/fwlink/p/?LinkID=236964) or other widely supported standards.

> [!Note]  
> As of December 2011, this topic has been archived. As a result, it is no longer actively maintained. For more information, see [Archived Content](https://msdn.microsoft.com/library/hh772377). For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](http://go.microsoft.com/fwlink/p/?linkid=204313).

 

Defines the direction of the text in the textbox. Read/write. **String**.

**Applies To**

[TextBox](msdn-online-vml-textbox-element.md)

**Tag Syntax**

&lt;v: *element* style="direction: *expression* "&gt;

**Remarks**

Values include:



| Value   | Description                                                                                |
|---------|--------------------------------------------------------------------------------------------|
| ltr     | Text is displayed left-to-right. Default.                                                  |
| rtl     | Text is displayed right-to-left.                                                           |
| context | Indicates that the **MSO-Direction-Alt** tag will be written out with the value "context". |



 

*Microsoft Office Extensions Attribute*

 

 



