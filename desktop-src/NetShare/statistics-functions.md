---
Description: The Windows operating system accumulates a set of operating statistics for workstations and servers from the time that the workstation or server service is started.
ms.assetid: 4e0217bf-7550-40a2-b47c-8e898a586005
title: Statistics Functions
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Statistics Functions

The Windows operating system accumulates a set of operating statistics for workstations and servers from the time that the workstation or server service is started. To retrieve these statistics, you can call the following network management statistics function.



| Function                                     | Description                                                                                 |
|----------------------------------------------|---------------------------------------------------------------------------------------------|
| [**NetStatisticsGet**](/windows/win32/Lmstats/nf-lmstats-netstatisticsget?branch=master) | Retrieves operating statistics for a service; supports the workstation and server services. |



 

The **NetStatisticsGet** function returns a [**STAT\_WORKSTATION\_0**](/windows/win32/Lmstats/ns-lmstats-_stat_workstation_0?branch=master) structure when workstation statistics are requested; the function returns a [**STAT\_SERVER\_0**](/windows/win32/Lmstats/ns-lmstats-_stat_server_0?branch=master) structure when server statistics are requested.

 

 


