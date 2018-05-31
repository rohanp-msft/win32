---
title: Creating a Recordset Object with the ADO API
description: Creating a Recordset Object with the ADO API
ms.assetid: 49152311-c6f0-40bf-a788-fbb89f8a6395
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Creating a Recordset Object with the ADO API

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](https://msdn.microsoft.com/library/windows/desktop/aa965362) for client side search and [Microsoft Search Server Express]( http://go.microsoft.com/fwlink/p/?linkid=258445) for server side search.

 

This code segment executes when the specified query language is the [SQL query language](sql-query-language.md). It sets several parameters and then uses the **CreateObject** function to create RS, a [Recordset](mdobjodbrec) object to represent the results of the query. It then executes the query using the [Open](mdmthrstopen) method of the RS **Recordset** object.


```VB
...
        Const adOpenForwardOnly = 0
        Connect = "provider=msidxs"
        CommandText = "SELECT Filename, Path, Size, Write FROM Scope('" + Chr(34) + Scope.Text + Chr(34) + "') WHERE " + QueryText.Text + " ORDER BY " + Sort.Text
...
        Set RS = CreateObject("ADODB.Recordset")
        RS.Open CommandText, Connect, adOpenForwardOnly
...
```



 

 



