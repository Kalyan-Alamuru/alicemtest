---
title: "SQLFreeStmt Mapping"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 267d95f2-4f0c-47ab-9411-5afe105215a2
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLFreeStmt Mapping
When an application calls **SQLFreeStmt** with an *Option* argument of SQL_DROP through an ODBC 3*.x* driver, the call to  
  
```  
SQLFreeStmt(hstmt, SQL_DROP)   
```  
  
 is mapped to  
  
```  
SQLFreeHandle(SQL_HANDLE_STMT,Handle)  
```  
  
 with the *Handle* argument set to the value in *hstmt*.