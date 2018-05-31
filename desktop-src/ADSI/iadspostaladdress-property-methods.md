---
title: IADsPostalAddress Property Methods
description: The property method of the IADsPostalAddress interface sets the property described in the following table. For more information, see Interface Property Methods.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\mbaldwin
ms.assetid: f7e61c69-f3a6-4ca6-a276-3cd859252571
ms.prod: windows-server-dev
ms.technology: active-directory-domain-services
ms.tgt_platform: multiple
keywords:
- IADsPostalAddress Property Methods ADSI
topic_type:
- apiref
api_name:
- IADsPostalAddress Property Methods
- IADsPostalAddress.PostalAddress
- IADsPostalAddress.get_PostalAddress
- IADsPostalAddress.put_PostalAddress
api_location:
- Activeds.dll
api_type:
- COM
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# IADsPostalAddress Property Methods

The property method of the [**IADsPostalAddress**](/windows/win32/Iads/nn-iads-iadspostaladdress?branch=master) interface sets the property described in the following table. For more information, see [Interface Property Methods](interface-property-methods.md).

## Properties

<dl> <dt>

**PostalAddress**
</dt> <dd> <dl>

An array of six strings holding the postal address of the user.

<dt>

Access type: Read/write
</dt> <dt>

Scripting data type: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] VARIANT* retVal
);
HRESULT put_PostalAddress(
  [in] VARIANT vPostalAddress
);
```


</dt> </dl> </dd> </dl>

 

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista<br/>                                                                |
| Minimum supported server<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID\_IADsPostalAddress is defined as 7ADECF29-4680-11D1-A3B4-00C04FB950DC<br/>    |



## See also

<dl> <dt>

[**IADsPostalAddress**](/windows/win32/Iads/nn-iads-iadspostaladdress?branch=master)
</dt> <dt>

[**ADS\_POSTALADDRESS**](/windows/win32/Iads/ns-iads-__midl___midl_itf_ads_0000_0000_0006?branch=master)
</dt> </dl>

 

 




