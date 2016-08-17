---
title: "SQLParamOptions Mapping"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 57ed65f6-9620-4738-b331-19d2a2b5cae4
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLParamOptions Mapping
When an application calls **SQLParamOptions** through an ODBC 3*.x* driver, the call  
  
```  
SQLParamOptions(hstmt, crow, piRow);  
```  
  
 will be mapped to two calls of **SQLSetStmtAttr** as follows:  
  
```  
SQLSetStmtAttr(hstmt, SQL_ATTR_PARAMSET_SIZE, crow, 0);  
SQLSetStmtAttr(hstmt, SQL_ATTR_PARAMS_PROCESSED_PTR, piRow, 0);  
```