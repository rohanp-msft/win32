---
Description: Sent when a set of DVD navigation commands are starting.
ms.assetid: 9cdcb211-a9e3-4a15-81bd-7ada2b9d823a
title: EC\_DVD\_BeginNavigationCommands
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# EC\_DVD\_BeginNavigationCommands

Sent when a set of DVD navigation commands are starting.

## Parameters

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

A value from the [**DVD\_NavCmdType**](/windows/win32/strmif/ne-strmif-tagdvd_navcmdtype?branch=master) enumeration.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## Remarks

This event is disabled by default. To enable this event, call [**IDvdControl2::SetOption**](/windows/win32/Strmif/nf-strmif-idvdcontrol2-setoption?branch=master) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.

## Requirements



|                   |                                                                                                          |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdevcode.h (include Dshow.h)</dt> </dl> |



## See also

<dl> <dt>

[DVD Applications](dvd-applications.md)
</dt> <dt>

[DVD Event Notification Codes](dvd-notification-codes.md)
</dt> <dt>

[Event Notification in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



