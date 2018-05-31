# [Function Discovery](fd-portal.md)
## [About Function Discovery](about-function-discovery.md)
### [Architectural Description](architectural-description.md)
### [Unifying the Discovery Process](unifying-the-discovery-process.md)
### [Function Instances](function-objects.md)
### [Function Discovery Categories](function-discovery-categories.md)
### [Function Discovery Queries](function-discovery-queries.md)
### [Category Metadata Manifests](category-metadata-manifests.md)
### [Constraints](constraints.md)
### [Built-in Providers](built-in-providers.md)
#### [NetBIOS Provider](netbios-provider.md)
#### [PnP Provider](pnp-provider.md)
#### [Registry Provider](registry-provider.md)
#### [SSDP Provider](ssdp-provider.md)
#### [WSD Provider](wsd-provider.md)
## [Using Function Discovery](using-function-discovery.md)
### [Retrieving all Function Instances in a Category](retrieving-all-function-instances-in-a-category.md)
### [Using the Function Discovery Browser](using-the-function-discovery-browser.md)
### [Function Discovery Sample](function-discovery-sample.md)
## [Function Discovery Reference](function-discovery-reference.md)
### [Function Discovery Constants](function-discovery-constants.md)
#### [Category Definitions](category-definitions.md)
#### [Constraint Definitions](constraint-definitions.md)
#### [Key Definitions](key-definitions.md)
##### [General PKEYs](general-pkeys.md)
##### [PnP-X Provider PKEYs](pnp-x-provider-pkeys.md)
##### [SSDP Provider PKEYs](ssdp-provider-pkeys.md)
##### [WCN Provider PKEYs](wcn-provider-pkeys.md)
##### [WNet Provider PKEYs](wnet-provider-pkeys.md)
##### [WSD Provider PKEYs](wsd-provider-pkeys.md)
#### [Subcategory Definitions](subcategory-definitions.md)
### [Function Discovery Enumerations](function-discovery-enumerations.md)
#### [PropertyConstraint](/windows/win32/FunctionDiscoveryConstraints/ne-functiondiscoveryconstraints-tagpropertyconstraint?branch=master)
#### [QueryUpdateAction](/windows/win32/FunctionDiscoveryAPI/ne-functiondiscoveryapi-tagqueryupdateaction?branch=master)
#### [SystemVisibilityFlags](/windows/win32/FunctionDiscoveryAPI/ne-functiondiscoveryapi-tagsystemvisibilityflags?branch=master)
### [Function Discovery Interfaces](function-discovery-interfaces.md)
#### [IFunctionDiscovery](/windows/win32/FunctionDiscoveryAPI/nn-functiondiscoveryapi-ifunctiondiscovery?branch=master)
##### [AddInstance Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctiondiscovery-addinstance?branch=master)
##### [CreateInstanceCollectionQuery Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctiondiscovery-createinstancecollectionquery?branch=master)
##### [CreateInstanceQuery Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctiondiscovery-createinstancequery?branch=master)
##### [GetInstance Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctiondiscovery-getinstance?branch=master)
##### [GetInstanceCollection Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctiondiscovery-getinstancecollection?branch=master)
##### [RemoveInstance Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctiondiscovery-removeinstance?branch=master)
#### [IFunctionDiscoveryNotification](/windows/win32/FunctionDiscoveryNotification/nn-functiondiscoveryapi-ifunctiondiscoverynotification?branch=master)
##### [OnError Method](ifunctiondiscoverynotification-onerror.md)
##### [OnEvent Method](ifunctiondiscoverynotification-onevent.md)
##### [OnUpdate Method](ifunctiondiscoverynotification-onupdate-method.md)
#### [IFunctionInstance](/windows/win32/FunctionDiscoveryAPI/nn-functiondiscoveryapi-ifunctioninstance?branch=master)
##### [GetCategory Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctioninstance-getcategory?branch=master)
##### [GetID Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctioninstance-getid?branch=master)
##### [GetProviderInstanceID Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctioninstance-getproviderinstanceid?branch=master)
##### [OpenPropertyStore Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctioninstance-openpropertystore?branch=master)
##### [QueryService Method](/windows/win32/FunctionDiscoveryAPI/?branch=master)
#### [IFunctionInstanceCollection](/windows/win32/FunctionDiscoveryAPI/nn-functiondiscoveryapi-ifunctioninstancecollection?branch=master)
##### [Add Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctioninstancecollection-add?branch=master)
##### [Delete Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctioninstancecollection-delete?branch=master)
##### [DeleteAll Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctioninstancecollection-deleteall?branch=master)
##### [Get Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctioninstancecollection-get?branch=master)
##### [GetCount Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctioninstancecollection-getcount?branch=master)
##### [Item Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctioninstancecollection-item?branch=master)
##### [Remove Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctioninstancecollection-remove?branch=master)
#### [IFunctionInstanceCollectionQuery](/windows/win32/FunctionDiscoveryAPI/nn-functiondiscoveryapi-ifunctioninstancecollectionquery?branch=master)
##### [AddPropertyConstraint Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctioninstancecollectionquery-addpropertyconstraint?branch=master)
##### [AddQueryConstraint Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctioninstancecollectionquery-addqueryconstraint?branch=master)
##### [Execute Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctioninstancecollectionquery-execute?branch=master)
#### [IFunctionInstanceQuery](/windows/win32/FunctionDiscoveryAPI/nn-functiondiscoveryapi-ifunctioninstancequery?branch=master)
##### [Execute Method](/windows/win32/FunctionDiscoveryAPI/nf-functiondiscoveryapi-ifunctioninstancequery-execute?branch=master)
### [Function Discovery Glossary](function-discovery-glossary.md)
## [Function Discovery Providers](portal-providers.md)
### [About Function Discovery Providers](about-function-discovery-providers.md)
#### [Provider Manifest Entries](provider-manifest-entries.md)
### [Using Function Discovery Providers](using-function-discovery-providers.md)
#### [Function Discovery Provider Sample](function-discovery-provider-sample.md)
### [Function Discovery Provider Reference](function-discovery-provider-reference.md)
#### [Function Discovery Provider Interfaces](function-discovery-provider-interfaces.md)
##### [IFunctionDiscoveryProvider](/windows/win32/FunctionDiscoveryProvider/nn-functiondiscoveryprovider-ifunctiondiscoveryprovider?branch=master)
###### [EndQuery Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-endquery?branch=master)
###### [Initialize Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-initialize?branch=master)
###### [InstancePropertyStoreFlush Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-instancepropertystoreflush?branch=master)
###### [InstancePropertyStoreOpen Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-instancepropertystoreopen?branch=master)
###### [InstancePropertyStoreValidateAccess Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-instancepropertystorevalidateaccess?branch=master)
###### [InstanceQueryService Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-instancequeryservice?branch=master)
###### [InstanceReleased Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-instancereleased?branch=master)
###### [Query Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-query?branch=master)
##### [IFunctionDiscoveryProviderFactory](/windows/win32/FunctionDiscoveryProvider/nn-functiondiscoveryprovider-ifunctiondiscoveryproviderfactory?branch=master)
###### [CreateInstance Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-ifunctiondiscoveryproviderfactory-createinstance?branch=master)
###### [CreateFunctionInstanceCollection Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-ifunctiondiscoveryproviderfactory-createfunctioninstancecollection?branch=master)
###### [CreatePropertyStore Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-ifunctiondiscoveryproviderfactory-createpropertystore?branch=master)
##### [IFunctionDiscoveryProviderQuery](/windows/win32/FunctionDiscoveryProvider/nn-functiondiscoveryprovider-ifunctiondiscoveryproviderquery?branch=master)
###### [GetPropertyConstraints Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-ifunctiondiscoveryproviderquery-getpropertyconstraints?branch=master)
###### [GetQueryConstraints Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-ifunctiondiscoveryproviderquery-getqueryconstraints?branch=master)
###### [IsInstanceQuery Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-ifunctiondiscoveryproviderquery-isinstancequery?branch=master)
###### [IsSubcategoryQuery Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-ifunctiondiscoveryproviderquery-issubcategoryquery?branch=master)
##### [IFunctionDiscoveryServiceProvider](/windows/win32/FunctionDiscoveryProvider/nn-functiondiscoveryprovider-ifunctiondiscoveryserviceprovider?branch=master)
###### [Initialize Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-ifunctiondiscoveryserviceprovider-initialize?branch=master)
##### [IProviderProperties](/windows/win32/FunctionDiscoveryProvider/nn-functiondiscoveryprovider-iproviderproperties?branch=master)
###### [GetAt Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-iproviderproperties-getat?branch=master)
###### [GetCount Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-iproviderproperties-getcount?branch=master)
###### [GetValue Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-iproviderproperties-getvalue?branch=master)
###### [SetValue Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-iproviderproperties-setvalue?branch=master)
##### [IProviderPropertyConstraintCollection](/windows/win32/FunctionDiscoveryProvider/nn-functiondiscoveryprovider-iproviderpropertyconstraintcollection?branch=master)
###### [Get Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-iproviderpropertyconstraintcollection-get?branch=master)
###### [GetCount Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-iproviderpropertyconstraintcollection-getcount?branch=master)
###### [Item Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-iproviderpropertyconstraintcollection-item?branch=master)
###### [Next Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-iproviderpropertyconstraintcollection-next?branch=master)
###### [Reset Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-iproviderpropertyconstraintcollection-reset?branch=master)
###### [Skip Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-iproviderpropertyconstraintcollection-skip?branch=master)
##### [IProviderPublishing](/windows/win32/FunctionDiscoveryProvider/nn-functiondiscoveryprovider-iproviderpublishing?branch=master)
###### [CreateInstance Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-iproviderpublishing-createinstance?branch=master)
###### [RemoveInstance Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-iproviderpublishing-removeinstance?branch=master)
##### [IProviderQueryConstraintCollection](/windows/win32/FunctionDiscoveryProvider/nn-functiondiscoveryprovider-iproviderqueryconstraintcollection?branch=master)
###### [Get Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-iproviderqueryconstraintcollection-get?branch=master)
###### [GetCount Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-iproviderqueryconstraintcollection-getcount?branch=master)
###### [Item Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-iproviderqueryconstraintcollection-item?branch=master)
###### [Next Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-iproviderqueryconstraintcollection-next?branch=master)
###### [Reset Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-iproviderqueryconstraintcollection-reset?branch=master)
###### [Skip Method](/windows/win32/FunctionDiscoveryProvider/nf-functiondiscoveryprovider-iproviderqueryconstraintcollection-skip?branch=master)
# [PnP-X](pnp-x.md)
## [Windows Rally Technologies](windows-rally-technologies.md)
## [PnP-X Association Database Reference](pnp-x-association-database-reference.md)
### [IPNPXAssociation](/windows/win32/pnpxassoc/nn-pnpxassoc-ipnpxassociation?branch=master)
#### [Associate Method](/windows/win32/pnpxassoc/nf-pnpxassoc-ipnpxassociation-associate?branch=master)
#### [Delete Method](/windows/win32/pnpxassoc/nf-pnpxassoc-ipnpxassociation-delete?branch=master)
#### [Unassociate Method](/windows/win32/pnpxassoc/nf-pnpxassoc-ipnpxassociation-unassociate?branch=master)
### [IPNPXDeviceAssociation](/windows/win32/pnpxassoc/nn-pnpxassoc-ipnpxdeviceassociation?branch=master)
#### [Associate Method](/windows/win32/pnpxassoc/nf-pnpxassoc-ipnpxdeviceassociation-associate?branch=master)
#### [Delete Method](/windows/win32/pnpxassoc/nf-pnpxassoc-ipnpxdeviceassociation-delete?branch=master)
#### [Unassociate Method](/windows/win32/pnpxassoc/nf-pnpxassoc-ipnpxdeviceassociation-unassociate?branch=master)
