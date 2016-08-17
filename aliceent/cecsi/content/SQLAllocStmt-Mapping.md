---
title: "SQLAllocStmt Mapping"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a2449dbb-1b6c-4b49-81b9-ebdddd4442fd
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLAllocStmt Mapping
When an application calls **SQLAllocStmt** through an ODBC 3*.x* driver, the call to:  
  
```  
SQLAllocStmt(hdbc, phstmt)  
```  
  
 is mapped to **SQLAllocHandle** by the Driver Manager in the driver as follows:  
  
```  
SQLAllocHandle(SQL_HANDLE_STMT, InputHandle, OutputHandlePtr)  
```  
  
 with *InputHandle* set to *hdbc* and *OutputHandlePtr* set to *phstmt*.