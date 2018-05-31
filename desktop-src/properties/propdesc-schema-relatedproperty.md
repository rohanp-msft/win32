---
Description: New for Windows 7. Identifies a property that is related to the property defined in the property description file.
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# relatedProperty

New for Windows 7. Identifies a property that is related to the property defined in the property description file. There can be as many [relatedProperty](shell.propdesc_schema_relatedProperty) elements within a [relatedPropertyInfo](shell.propdesc_schema_relatedPropertyInfo) as needed.

## Syntax


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
        <xs:attribute name="propertyName" type="canonical-name" use="required"/>
    </xs:complexType>
</xs:element>
```



## Element Information



| Parent Element                                                   | Child Elements |
|------------------------------------------------------------------|----------------|
| [relatedPropertyInfo](shell.propdesc_schema_relatedPropertyInfo) | None           |



 

## Attributes



| Attribute        | Description                                                        |
|------------------|--------------------------------------------------------------------|
| relationshipName | Public. Required. The canonical name of the property relationship. |
| propertyName     | Public. Required. The canonical name of the related property.      |



 

## Remarks

This element enables you to map one property to another. For example, you can map the text of your custom property, Fabrikam.StorageCapacity, to System.Capacity:


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 


