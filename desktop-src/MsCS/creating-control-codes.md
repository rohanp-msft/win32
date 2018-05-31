---
title: Creating Control Codes
description: If you are creating a resource type, you may need to create one or more control codes to expose specialized operations to other developers.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: dc1191d0-9364-40a3-abca-c59aa9f5b3aa
ms.prod: windows-server-dev
ms.technology: failover-clustering
ms.tgt_platform: multiple
keywords:
- control codes Failover Cluster ,creating
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# Creating Control Codes

If you are creating a [resource type](resource-types.md), you may need to create one or more [control codes](about-control-codes.md) to expose specialized operations to other developers. By supporting these custom control codes in your [resource DLL](resource-dlls.md), you allow programmers to initiate the operations with [**ClusterResourceControl**](/windows/previous-versions/ClusAPI/nf-clusapi-clusterresourcecontrol?branch=master) or [**ClusterResourceTypeControl**](/windows/previous-versions/ClusAPI/nf-clusapi-clusterresourcetypecontrol?branch=master).

For example, suppose you create a resource type for an application that generates a log file. You want other programmers to be able to read and change the location of the log file in their applications. To accomplish this, you could define control codes such as:

MYAPPNAME\_GET\_LOG\_FILE\_LOCATION

MYAPPNAME\_SET\_LOG\_FILE\_LOCATION

Programmers would use the control codes as [**ClusterResourceControl**](/windows/previous-versions/ClusAPI/nf-clusapi-clusterresourcecontrol?branch=master) or [**ClusterResourceTypeControl**](/windows/previous-versions/ClusAPI/nf-clusapi-clusterresourcetypecontrol?branch=master) parameters. The [Cluster service](cluster-service.md) would pass the control code to your resource DLL, which would handle the operation (the [Resource Monitor](resource-monitor.md), or course, would not know how to handle it).

**To create a user-defined control code**

1.  Review [control code architecture](control-code-architecture.md).
2.  Use the [**CLUSCTL\_USER\_CODE**](/windows/previous-versions/ClusAPI/nf-clusapi-clusctl_user_code?branch=master) macro to create the control code.
3.  Implement the control code in the [**ResourceControl**](/windows/previous-versions/ResApi/nc-resapi-presource_control_routine?branch=master) and [**ResourceTypeControl**](/windows/previous-versions/ResApi/nc-resapi-presource_type_control_routine?branch=master) entry points of your resource DLL.
4.  Document the procedures for using the control code, especially what the contents of the [**ClusterResourceControl**](/windows/previous-versions/ClusAPI/nf-clusapi-clusterresourcecontrol?branch=master) and [**ClusterResourceTypeControl**](/windows/previous-versions/ClusAPI/nf-clusapi-clusterresourcetypecontrol?branch=master) input and output buffers should be.

## Example

The following code creates three control codes for a fictional resource type called "ServiceX".


```C++
#include <windows.h>
#include "ClusDocEx.h"

//////////////////////////////////////////////////////////////////////
//  DEFINE CONTROL CODES
//////////////////////////////////////////////////////////////////////

//  Object code

#define SERVICEX_OBJECT_CODE 221

//  Function codes

typedef enum SERVICEX_FUNCTION_CODES
 {
  SVCX_GET_LOGFILE_LOCATION = 22101,
  SVCX_SET_LOGFILE_LOCATION = 22102
 }
 SERVICEX_FUNCTION_CODES;


//  Create the control codes.

typedef enum SERVICEX_CONTROL_CODES
 {
  SERVICEX_GET_LOGFILE_LOCATION = CLUSCTL_USER_CODE( SVCX_GET_LOGFILE_LOCATION, SERVICEX_OBJECT_CODE ) | CLUS_ACCESS_READ,

  SERVICEX_SET_LOGFILE_LOCATION = CLUSCTL_USER_CODE( SVCX_SET_LOGFILE_LOCATION, SERVICEX_OBJECT_CODE ) | CLUS_ACCESS_ANY

 }
 SERVICEX_CONTROL_CODES; 


//--------------------------------------------------------------------
//  TODO:  Support these control codes in the ResourceControl and 
//         ResourceTypeControl entry points of the "ServiceX" 
//         resource DLL.  Document how the codes should be used.
//--------------------------------------------------------------------

//////////////////////////////////////////////////////////////////////
```



 

 



