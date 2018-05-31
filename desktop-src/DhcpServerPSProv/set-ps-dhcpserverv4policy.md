---
title: Set method of the PS\_DhcpServerv4Policy class
description: Sets the properties of an existing policy either at the server level or at the specified scope level.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 141b9122-8ff5-42ee-b9c1-509c82e8f62b
ms.prod: windows-server-dev
ms.technology:
- dhcp-server
- windows-management-instrumentation
ms.tgt_platform: multiple
keywords:
- Set method
- Set method, PS_DhcpServerv4Policy class
- PS_DhcpServerv4Policy class, Set method
topic_type:
- apiref
api_name:
- PS_DhcpServerv4Policy.Set
api_location:
- DhcpServerPsProvider.dll
api_type:
- COM
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# Set method of the PS\_DhcpServerv4Policy class

Sets the properties of an existing policy either at the server level or at the specified scope level.

## Syntax


```mof
uint32 Set(
  [in]  string             ComputerName,
  [in]  string             Description,
  [in]  string             Name,
  [in]  string             ScopeId,
  [in]  boolean            Enabled,
  [in]  datetime           LeaseDuration,
  [in]  string             Fqdn[],
  [in]  string             MacAddress[],
  [in]  string             UserClass[],
  [in]  string             SubscriberId[],
  [in]  string             NewName,
  [in]  string             ClientId[],
  [in]  boolean            PassThru,
  [in]  uint16             ProcessingOrder,
  [in]  string             RelayAgent[],
  [in]  string             RemoteId[],
  [in]  string             CircuitId[],
  [in]  string             Condition,
  [in]  string             VendorClass[],
  [out] DhcpServerv4Policy cmdletOutput
);
```



## Parameters

<dl> <dt>

*ComputerName* \[in\]
</dt> <dd>

DNS name or IP address of the target computer running the DHCP server service.

</dd> <dt>

*Description* \[in\]
</dt> <dd>

Description string to be set on the policy

</dd> <dt>

*Name* \[in\]
</dt> <dd>

Name of the policy to be modified

</dd> <dt>

*ScopeId* \[in\]
</dt> <dd>

Scope identifier (in IPv4 address format) of the scope which contains the policy. If not specified, server level policy is modified.

</dd> <dt>

*Enabled* \[in\]
</dt> <dd>

Enable/Disable policy. Valid values are True, False.

</dd> <dt>

*LeaseDuration* \[in\]
</dt> <dd>

Lease duration to be set for clients matching the policy.

**Windows Server 2012:** This parameter is supported beginning with Windows Server 2012 R2.

</dd> <dt>

*Fqdn* \[in\]
</dt> <dd>

"The comparator to use, and values to compare Fqdn with.

Specify the comparator in the first element and values in the subsequent elements are values. There are four possible values for the comparator; **EQ**, **NE**, **Isl**, and **Insl**

For comparators **Isl** and **Insl** only a blank value is acceptable.

If comparators **EQ** or **NE** are used: If the last character in a value-element is an asterisk (\*), the subsequent characters are treated as wild-cards for the comparison. If the first character in a value-element is an asterisk (\*), the preceding characters are treated as wild cards for comparison.

Value elements can be followed by another comparator, either **EQ** or **NE**, which is followed by another set of values. The values following the EQ operator will be treated as multiple assertions which are ORed. The values following the NE operator will be treated as multiple assertions which are ANDed.

**Windows Server 2012:** This parameter is supported beginning with Windows Server 2012 R2.

</dd> <dt>

*MacAddress* \[in\]
</dt> <dd>

The comparator to use and values to compare MAC Address in the client request with. The first element is the comparator (EQ, NE), and subsequent elements are values. If the last character in a value is an asterisk (\*), the subsequent characters are treated as wild-cards for the comparison. Values can again be followed by another comparator (EQ, NE) which is followed by another set of values. Input format is a hex string with or without hyphen separation. A trailing wildcard character can be present to indicate partial match. For example. 00-1F-3B-7C-B7-89, 00-1F-3B-7C-B7-\*, 001F3B7CB789. Output format is hex string with hyphen separation. The values following the EQ operator will be treated as multiple assertions which are joined with a bitwise **OR** combination. The values following the NE operator will be treated as multiple assertions which are joined with a bitwise **AND** combination.

</dd> <dt>

*UserClass* \[in\]
</dt> <dd>

The comparator to use and user class values to compare with the user class field in the client request. The first element to be specified is the comparator {EQ, NE} and the subsequent elements are values. If the last character in the value is an asterisk (\*), the subsequent characters are treated as wild-cards for the comparison. Values can again be followed by another comparator (EQ, NE) which is followed by another set of values. Values to be specified are the user class names which are already existing on the server. The format of the value should be a hex string prepended with 0x. The values following the EQ operator are treated as multiple assertions which are joined with a bitwise **OR** combination. The values following the NE operator are treated as multiple assertions which are joined with a bitwise **AND** combination.

</dd> <dt>

*SubscriberId* \[in\]
</dt> <dd>

The comparator to use and values to compare subscriber id suboption with. The first element is the comparator (EQ, NE), and followed by a single value. No wildcard characters are allowed. Value can again be followed by another comparator (EQ, NE) which is followed by another value. Input format is a hex string with or without hyphen separation.

</dd> <dt>

*NewName* \[in\]
</dt> <dd>

New name to be set for the policy

</dd> <dt>

*ClientId* \[in\]
</dt> <dd>

The comparator to use and values to compare client identifier with. The first element is the comparator (EQ, NE), and subsequent elements are values. If the last character in a value is an asterisk (\*), the subsequent characters are treated as wild-cards for the comparison. Values can again be followed by another comparator (EQ, NE) which is followed by another set of values. Input format is a hex string with or without hyphen separation. Output format is hex string with hyphen separation. The values following the EQ operator will be treated as multiple assertions which are joined with a bitwise **OR** combination. The values following the NE operator will be treated as multiple assertions which are joined with a bitwise **AND** combination. Example { EQ, 00-11-22-33-44-55, AA-BB-CC-DD-EE\*}

</dd> <dt>

*PassThru* \[in\]
</dt> <dd>

If this parameter is specified, the cmdlet returns the PowerShell object which is modified.

</dd> <dt>

*ProcessingOrder* \[in\]
</dt> <dd>

The order of this policy with respect to other policies in the scope or server. The server will process the policies in the specified order while evaluating client requests vis-a-vis the configured policies.

</dd> <dt>

*RelayAgent* \[in\]
</dt> <dd>

The comparator to use and values to compare relay agent information with. The first element is the comparator (EQ, NE), and subsequent elements are values. No wildcard characters are allowed. Values can again be followed by another comparator (EQ, NE) which is followed by another set of values. Input format is a hex string with or without hyphen separation.

</dd> <dt>

*RemoteId* \[in\]
</dt> <dd>

The comparator to use and values to compare remote id suboption with. The first element is the comparator (EQ, NE) followed by a single value. No wildcard characters are allowed. Value can again be followed by another comparator (EQ, NE) which is followed by another value. Input format for the value is a hex string with or without hyphen separation.

</dd> <dt>

*CircuitId* \[in\]
</dt> <dd>

The comparator to use and values to compare circuit id suboption with. The first element is the comparator (EQ, NE) followed by a single value. No wildcard characters are allowed. Value can again be followed by another comparator (EQ, NE) which is followed by another value. Input format for the value is a hex string with or without hyphen separation.

</dd> <dt>

*Condition* \[in\]
</dt> <dd>

The logical operator between conditions in case multiple conditions are specified. Valid values are **AND**, and **OR**.

<dt>

<span id="And"></span><span id="and"></span><span id="AND"></span>

**And** ("And")


</dt> <dd></dd> <dt>

<span id="Or"></span><span id="or"></span><span id="OR"></span>

**Or** ("Or")


</dt> <dd></dd> </dl> </dd> <dt>

*VendorClass* \[in\]
</dt> <dd>

The comparator to use and vendor class values to compare with the vendor class field in the client request. The first element is the comparator (EQ, NE), and subsequent elements are values. If the last character in a value is an asterisk (\*), the subsequent characters are treated as wild-cards for the comparison. Values can again be followed by another comparator (EQ/NE) which is followed by another set of values. Values to be specified are the vendor class names which are already existing on the server. The format of the value should be a hex string prepended with 0x. The values following the EQ operator are treated as multiple assertions which are joined with a bitwise **OR** combination. The values following the NE operator are treated as multiple assertions which are joined with a bitwise **AND** combination.

</dd> <dt>

*cmdletOutput* \[out\]
</dt> <dd>

An embedded instance of the [**DhcpServerv4Policy**](dhcpserverv4policy.md) class.

</dd> </dl>

## Requirements



|                                     |                                                                                                     |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                                           |
| Minimum supported server<br/> | Windows Server 2012<br/>                                                                      |
| Namespace<br/>                | Root\\Microsoft\\Windows\\DHCP<br/>                                                           |
| MOF<br/>                      | <dl> <dt>DhcpServerPsProvider.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DhcpServerPsProvider.dll</dt> </dl> |



## See also

<dl> <dt>

[**PS\_DhcpServerv4Policy**](ps-dhcpserverv4policy.md)
</dt> </dl>

 

 




