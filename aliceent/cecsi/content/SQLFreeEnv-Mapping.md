---
title: "SQLFreeEnv Mapping"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c0f76455-d072-4bae-bee7-452277dfa479
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLFreeEnv Mapping
When an application calls **SQLFreeEnv** through an ODBC 3*.x* driver, the call to  
  
```  
SQLFreeEnv(henv)   
```  
  
 is mapped to  
  
```  
SQLFreeHandle(SQL_HANDLE_ENV,Handle)  
```  
  
 with the *Handle* argument set to the value in *henv*.