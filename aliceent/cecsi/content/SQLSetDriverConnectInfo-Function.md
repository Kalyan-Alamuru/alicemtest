---
title: "SQLSetDriverConnectInfo Function"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bfd4dfc2-fbca-4ef3-81e5-2706f2389256
caps.latest.revision: 11
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLSetDriverConnectInfo Function
**Conformance**  
 Version Introduced: ODBC 3.81 Standards Compliance: ODBC  
  
 **Summary**  
 **SQLSetDriverConnectInfo** is used to set the connection string into the connection info token for an application’s **SQLDriverConnect** call.  
  
## Syntax  
  
```  
SQLRETURN SQLSetDriverConnectInfo(  
                SQLHDBC_INFO_TOKEN   hDbcInfoToken,  
                WCHAR *              InConnectionString,  
                SQLSMALLINT          StringLength1 );  
```  
  
## Arguments  
 *TokenHandle*  
 [Input] Token handle.  
  
 *InConnectionString*  
 [Input] A full connection string (see the syntax in "Comments" in [SQLDriverConnect](../content/SQLDriverConnect-Function.md)), a partial connection string, or an empty string.  
  
 *StringLength1*  
 [Input] Length of **InConnectionString*, in characters if the string is Unicode, or bytes if string is ANSI or DBCS.  
  
## Returns  
 SQL_SUCCESS, SQL_SUCCESS_WITH_INFO, SQL_ERROR, or SQL_INVALID_HANDLE.  
  
## Diagnostics  
 Same as [SQLDriverConnect](../content/SQLDriverConnect-Function.md) related to any input validation error, except that the Driver Manager will use a **HandleType** of SQL_HANDLE_DBC_INFO_TOKEN and a **Handle** of *hDbcInfoToken*.  
  
## Remarks  
 Whenever a driver returns SQL_ERROR or SQL_INVALID_HANDLE, the Driver Manager returns the error to the application (in [SQLConnect](../content/SQLConnect-Function.md) or [SQLDriverConnect](../content/SQLDriverConnect-Function.md)).  
  
 Whenever a driver returns SQL_SUCCESS_WITH_INFO, the Driver Manager will obtain the diagnostic information from *hDbcInfoToken*, and return SQL_SUCCESS_WITH_INFO to the application in [SQLConnect](../content/SQLConnect-Function.md) and [SQLDriverConnect](../content/SQLDriverConnect-Function.md).  
  
 Applications should not call this function directly. An ODBC driver that supports driver-aware connection pooling must implement this function.  
  
 Include sqlspi.h for ODBC driver development.  
  
## See Also  
 [Developing an ODBC Driver](../content/Developing-an-ODBC-Driver.md)   
 [Driver-Aware Connection Pooling](../content/Driver-Aware-Connection-Pooling.md)   
 [Developing Connection-Pool Awareness in an ODBC Driver](../content/Developing-Connection-Pool-Awareness-in-an-ODBC-Driver.md)