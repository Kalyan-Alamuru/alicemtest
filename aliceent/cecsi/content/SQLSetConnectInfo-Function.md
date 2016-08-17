---
title: "SQLSetConnectInfo Function"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0782a1c3-c5d1-499b-a8ba-134162db9990
caps.latest.revision: 16
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLSetConnectInfo Function
**Conformance**  
 Version Introduced: ODBC 3.81 Standards Compliance: ODBC  
  
 **Summary**  
 **SQLSetConnectInfo** is used to set the data source, user ID, and password into the connection info token for an application’s [SQLConnect](../content/SQLConnect-Function.md) call.  
  
## Syntax  
  
```  
SQLRETURN  SQLSetConnectInfo(  
                SQLHDBC_INFO_TOKEN   TokenHandle,  
                WCHAR *              ServerName,  
                SQLSMALLINT          NameLength1,  
                WCHAR *              UserName,  
                SQLSMALLINT          NameLength2,  
                WCHAR *              Authentication,  
                SQLSMALLINT          NameLength3 );  
```  
  
## Arguments  
 *TokenHandle*  
 [Input] Token handle.  
  
 *ServerName*  
 [Input] Data source name. The data might be located on the same computer as the program, or on another computer somewhere on a network. For information about how an application chooses a data source, see [Choosing a Data Source or Driver](../content/Choosing-a-Data-Source-or-Driver.md).  
  
 *NameLength1*  
 [Input] Length of **ServerName* in characters.  
  
 *UserName*  
 [Input] User identifier.  
  
 *NameLength2*  
 [Input] Length of **UserName* in characters.  
  
 *Authentication*  
 [Input] Authentication string (typically the password).  
  
 *NameLength3*  
 [Input] Length of **Authentication* in characters.  
  
## Returns  
 SQL_SUCCESS, SQL_SUCCESS_WITH_INFO, SQL_ERROR, or SQL_INVALID_HANDLE.  
  
## Diagnostics  
 Same as [SQLConnect](../content/SQLConnect-Function.md) for input validation errors, except that the Driver Manager will use a **HandleType** of SQL_HANDLE_DBC_INFO_TOKEN and a **Handle** of *hDbcInfoToken*.  
  
## Remarks  
 Whenever a driver returns SQL_ERROR or SQL_INVALID_HANDLE, the Driver Manager returns the error to the application (in [SQLConnect](../content/SQLConnect-Function.md) or [SQLDriverConnect](../content/SQLDriverConnect-Function.md)).  
  
 Whenever a driver returns SQL_SUCCESS_WITH_INFO, the Driver Manager will obtain the diagnostic information from *hDbcInfoToken*, and return SQL_SUCCESS_WITH_INFO to the application in [SQLConnect](../content/SQLConnect-Function.md) and [SQLDriverConnect](../content/SQLDriverConnect-Function.md).  
  
 Applications should not call this function directly. An ODBC driver that supports driver-aware connection pooling must implement this function.  
  
 Include sqlspi.h for ODBC driver development.  
  
## See Also  
 [Developing an ODBC Driver](../content/Developing-an-ODBC-Driver.md)   
 [Driver-Aware Connection Pooling](../content/Driver-Aware-Connection-Pooling.md)   
 [Developing Connection-Pool Awareness in an ODBC Driver](../content/Developing-Connection-Pool-Awareness-in-an-ODBC-Driver.md)