---
title: "SQLRemoveDefaultDataSource Function"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLRemoveDefaultDataSource
apilocation: 
  - sqlsrv32.dll
apitype: dllExport
ms.assetid: db803266-57df-4864-a41b-901247549c1f
caps.latest.revision: 7
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLRemoveDefaultDataSource Function
**Conformance**  
 Version Introduced: ODBC 1.0, Deprecated  
  
 **Summary**  
 In ODBC 3.0, the **SQLRemoveDefaultDataSource** function has been replaced by a call to [SQLConfigDataSource](../content/SQLConfigDataSource-Function.md) with an *fRequest* argument of ODBC_REMOVE_DEFAULT_DSN. If an ODBC 2*.x* installation program calls this function, the ODBC installer will map it to the following **SQLConfigDataSource** call:  
  
```  
SQLConfigDataSource (NULL, ODBC_REMOVE_DEFAULT_DSN, NULL, NULL)  
```