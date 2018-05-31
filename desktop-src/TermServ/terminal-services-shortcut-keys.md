---
title: Remote Desktop Services Shortcut Keys
description: A list of the Remote Desktop Services shortcut keys.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 03a94323-2616-4f35-a5c0-3c238acb7693
ms.prod: windows-server-dev
ms.technology: remote-desktop-services
ms.tgt_platform: multiple
keywords:
- Remote Desktop Services Remote Desktop Services , shortcut keys
- Remote Desktop Services Remote Desktop Services , keyboard shortcuts
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# Remote Desktop Services Shortcut Keys

The following is a list of the Remote Desktop Services shortcut keys.

**Missing keys:  **

Many compact keyboards do not contain some of these keys. For example, many laptops do not have a dedicated BREAK key. However, they usually have keyboard shortcuts that replace dedicated keys. These key replacements are specified by the manufacturer of the keyboard, so you may need to look up key replacements in the documentation provided by your keyboard or laptop manufacturer.

There are two possible shortcut key combinations you can use on a remote desktop connection: the default Windows shortcut keys, or the shortcut keys originally designed for the remote desktop. You can set which shortcut keys you use on the local and remote machine through the Remote Desktop Connection client (ie, the dialog that appears when you click on the **Remote Desktop Connection** icon). From there, click **Show Options** (if you cannot see the options), and then click the **Local Resources** tab. In the **Apply Windows key combinations** drop-down, you have three options:

<dl> <dt>

<span id="On_this_computer"></span><span id="on_this_computer"></span><span id="ON_THIS_COMPUTER"></span>On this computer
</dt> <dd>

the default key combinations will work on your local machine only. You must use the alternate combinations on the remote desktop.

</dd> <dt>

<span id="On_the_remote_computer"></span><span id="on_the_remote_computer"></span><span id="ON_THE_REMOTE_COMPUTER"></span>On the remote computer
</dt> <dd>

The default key combinations will work only on the remote desktop. You must use the alternate combinations on the local machine. Note that once you close down the Remote Desktop Connection, your local machine will once again use the default windows shortcuts.

</dd> <dt>

<span id="Only_when_using_the_full_screen"></span><span id="only_when_using_the_full_screen"></span><span id="ONLY_WHEN_USING_THE_FULL_SCREEN"></span>Only when using the full screen
</dt> <dd>

The default key combinations will work on whichever machine has the full desktop; functionally, this means that the default key combinations work for the local machine, unless you have the Remote Desktop Connection window in full-screen mode.

</dd> </dl>

For more user information about Remote Desktop connection, See [Remote Desktop Connection: frequently asked questions](http://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Shortcut key</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CTRL+ALT+HOME<br/></td>
<td>Activates the <strong>connection</strong> bar.<br/></td>
</tr>
<tr class="even">
<td>CTRL+ALT+BREAK or one of these shortcuts:<br/>
<ul>
<li>CTRL+ALT+PAUSE<br/></li>
<li>CTRL+ALT+PRTSCN<br/></li>
<li>CTRL+ALT+FN+SCRLK<br/></li>
</ul></td>
<td>Switches the client between full-screen mode and window mode.<br/> If these shortcuts don't work, or the keys aren't available, you can try the following alternative:<br/>
<ul>
<li>Press CTRL+ALT+HOME, TAB, TAB, TAB, TAB, TAB, ENTER. This activates the <strong>connection</strong> bar, and then presses the <strong>Restore down</strong> button.<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>CTRL+ALT+END<br/></td>
<td>Brings up the <strong>Windows Security</strong> dialog box for the Remote Desktop Session Host (RD Session Host) (provides the same functionality as pressing CTRL+ALT+DEL on the local computer).<br/></td>
</tr>
</tbody>
</table>



 

The following table describes the standard Windows shortcut keys and their equivalent Remote Desktop shortcuts that are different. (For example, Ctrl+Z is generally the 'Undo' shortcut on both standard Windows and Remote Desktop.)



| Windows shortcut                                         | Remote Desktop shortcut            | Description                                                                             |
|----------------------------------------------------------|------------------------------------|-----------------------------------------------------------------------------------------|
| ALT+TAB<br/>                                       | ALT+PAGE UP<br/>             | Switches between programs from left to right.<br/>                                |
| ALT+SHIFT+TAB<br/>                                 | ALT+PAGE DOWN<br/>           | Switches between programs from right to left.<br/>                                |
|                                                          | ALT+INSERT<br/>              | Cycles through the programs in the order they were started.<br/>                  |
| Windows key<br/> or<br/> CTRL+ESC<br/> | ALT+HOME<br/>                | Displays the **Start** menu.<br/>                                                 |
| ALT+SPACE BAR<br/>                                 | ALT+DELETE<br/>              | Displays the **system** menu.<br/>                                                |
| ALT+PRINT SCREEN<br/>                              | CTRL+ALT+MINUS SIGN (-)<br/> | Places a snapshot of the active window, within the client, on the clipboard.<br/> |
| PRINT SCREEN<br/>                                  | CTRL+ALT+PLUS SIGN (+)<br/>  | Places a snapshot of the entire client windows area on the clipboard .<br/>       |



 

## Related topics

<dl> <dt>

[Remote Desktop Services](terminal-services-portal.md)
</dt> </dl>

 

 




