---
title: Example Code for Binding to the Users Container
description: This topic includes a code example that will bind to the users container in the current domain and return and IADsContainer interface for the container.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\mbaldwin
ms.assetid: 78524b05-f57a-4816-92eb-e37be74dd245
ms.prod: windows-server-dev
ms.technology: active-directory-domain-services
ms.tgt_platform: multiple
keywords:
- Active Directory examples Active Directory , binding to users container
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
---

# Example Code for Binding to the User's Container

The following C++ code example binds to the users container in the current domain and return and [**IADsContainer**](https://msdn.microsoft.com/library/aa705985) interface for the container. For more information about binding to well-known objects, see [Binding to Well-Known Objects Using WKGUID](binding-to-well-known-objects-using-wkguid.md).


```C++
//**********************************************************
//
//  GetUsersContainer()
//
//  Binds to the well-known Users container in the current domain 
//  with the current user credentials. GUID_USERS_CONTAINER_W is 
//  defined in NTDSAPI.H.
//
//*******************************************************************

HRESULT GetUsersContainer(IADsContainer **ppContainer)
{
    if(NULL == ppContainer)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADs *pRoot;

    *ppContainer = NULL;

    // Bind to the rootDSE object.
    hr = ADsOpenObject(L"LDAP://rootDSE",
                    NULL,
                    NULL,
                    ADS_SECURE_AUTHENTICATION,
                    IID_IADs,
                    (LPVOID*)&amp;pRoot);
    if(SUCCEEDED(hr))
    {
        VARIANT var;
        
        VariantInit(&amp;var);

        // Get the current domain DN.
        hr = pRoot->Get(CComBSTR("defaultNamingContext"), &amp;var);
        if(SUCCEEDED(hr))
        {
            // Build the binding string.
            LPWSTR pwszFormat = L"LDAP://<WKGUID=%s,%s>";
            LPWSTR pwszPath;

            pwszPath = new WCHAR[wcslen(pwszFormat) + 
                           wcslen(GUID_USERS_CONTAINER_W) + 
                           wcslen(var.bstrVal)];
            if(NULL != pwszPath)
            {
                swprintf_s(pwszPath, 
                         pwszFormat, 
                         GUID_USERS_CONTAINER_W,
                         var.bstrVal);

                // Bind to the object.
                hr = ADsOpenObject(pwszPath,
                                NULL,
                                NULL,
                                ADS_SECURE_AUTHENTICATION,
                                IID_IADsContainer,
                                (LPVOID*)ppContainer);

                delete pwszPath;
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }

            VariantClear(&amp;var);        
        }

        pRoot->Release(); 
    }

    return hr;
}
```



 

 



