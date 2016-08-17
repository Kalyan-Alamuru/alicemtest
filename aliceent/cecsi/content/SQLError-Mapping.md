---
title: "SQLError Mapping"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 802ac711-7e5d-4152-9698-db0cafcf6047
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLError Mapping
When an application calls **SQLError** through an ODBC 3*.x* driver, the call to  
  
```  
SQLError(henv, hdbc, hstmt, szSqlState, pfNativeError, szErrorMsg, cbErrorMsgMax, pcbErrorMsg)   
```  
  
 is mapped to  
  
```  
SQLGetDiagRec(HandleType, Handle, RecNumber, szSqlstate, pfNativeErrorPtr, szErrorMsg, cbErrorMsgMax, pcbErrorMsg)  
```  
  
 with the *HandleType* argument set to the value SQL_HANDLE_ENV, SQL_HANDLE_DBC, or SQL_HANDLE_STMT, as appropriate, and the *Handle* argument set to the value in *henv*, *hdbc*, or *hstmt*, as appropriate. The *RecNumber* argument is determined by the Driver Manager.