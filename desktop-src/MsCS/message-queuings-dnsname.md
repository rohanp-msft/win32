---
title: DnsName
description: Contains the full DNS label associated with the message queuing resource.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: D4B213BB-DE8E-4A48-86CF-21C9BF605D96
ms.prod: windows-server-dev
ms.technology: failover-clustering
ms.tgt_platform: multiple
keywords:
- DnsName Failover Cluster , for message queuings
- DnsName Failover Cluster
topic_type:
- apiref
api_name:
- DnsName
api_type:
- NA
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# DnsName

Contains the full [*DNS*](d-gly.md#-wolf-domain-name-system-gly) label associated with the [message queuing](message-queuing.md) resource. The following table summarizes the attributes of the **DnsName** property.



| Attribute | Value                                                            |
|-----------|------------------------------------------------------------------|
| Data type | Null-terminated Unicode string                                   |
| Access    | [Read/write](read-write-properties.md)                          |
| Status    | Required                                                         |
| Structure | [**CLUSPROP\_SZ**](/windows/previous-versions/ClusAPI/?branch=master)                              |
| Maximum   | None (but see [Maximum Property Size](maximum-string-size.md).) |
| Default   | **NULL**                                                         |



 

## Remarks

The [**CLUSPROP\_SZ\_DECLARE**](/windows/previous-versions/ClusAPI/nf-clusapi-clusprop_sz_declare?branch=master) macro creates a [**CLUSPROP\_SZ**](/windows/previous-versions/ClusAPI/?branch=master) structure with an array of the correct size.

## Examples

The property value portion of a [property list](property-lists.md) entry for **DnsName** can be set with the following example code.


```C++
WCHAR szDnsNameData[]  = L"myDNS";
CLUSPROP_SZ_DECLARE(     DnsNameValue, sizeof( szDnsNameData ) / sizeof( WCHAR ) );

DnsNameValue.Syntax.dw = CLUSPROP_SYNTAX_LIST_VALUE_SZ;
DnsNameValue.cbLength  = sizeof( szDnsNameData );
StringCbCopy(            DnsNameValue.sz, 
                         DnsNameValue.cbLength, 
                         szDnsNameData );
```



## Requirements



|                                     |                                |
|-------------------------------------|--------------------------------|
| Minimum supported client<br/> | None supported<br/>      |
| Minimum supported server<br/> | Windows Server 2012<br/> |



## See also

<dl> <dt>

[Message Queuing Private Properties](message-queuing-private-properties.md)
</dt> <dt>

[**CLUSPROP\_SZ**](/windows/previous-versions/ClusAPI/?branch=master)
</dt> <dt>

[**CLUSPROP\_SZ\_DECLARE**](/windows/previous-versions/ClusAPI/nf-clusapi-clusprop_sz_declare?branch=master)
</dt> </dl>

 

 




