---
title: "SQLGetPoolID Function"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 95a8666a-ad68-4d89-bf65-f2cc797f8820
caps.latest.revision: 13
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLGetPoolID Function
**Conformance**  
 Version Introduced: ODBC 3.81 Standards Compliance: ODBC  
  
 **Summary**  
 **SQLGetPoolID** retrieves the pool ID.  
  
## Syntax  
  
```  
SQLRETURN  SQLGetPoolID (  
                SQLHDBC_INFO_TOKEN    hDbcInfoToken,  
                POOLID *              pPoolID );  
```  
  
## Arguments  
 *hDbcInfoToken*  
 [Input] Token handle that contains all connection information.  
  
 *pPoolID*  
 [Output] The pool ID, which is used to identify a set of connections that can be used interchangeably (possibly requiring an additional reset).  
  
## Returns  
 SQL_SUCCESS, SQL_SUCCESS_WITH_INFO, SQL_ERROR, or SQL_INVALID_HANDLE.  
  
## Diagnostics  
 When **SQLGetPoolID** returns SQL_ERROR or SQL_SUCCESS_WITH_INFO, the Driver Manager will use a **HandleType** of SQL_HANDLE_DBC_INFO_TOKEN and a **Handle** of *hDbcInfoToken*.  
  
## Remarks  
 **SQLGetPoolID** is used to obtain the pool ID given a set of connection information (from **SQLSetConnectAttrForDbcInfo**, **SQLSetDriverConnectInfo**, and **SQLSetConnectInfo**). This pool ID is used to identify a set of connections that can be used interchangeably (possibly requiring an additional reset). The pool ID will be used to identify the connection pool for that group of connections.  
  
 Whenever a driver returns SQL_ERROR or SQL_INVALID_HANDLE, the Driver Manager returns the error to the application (in [SQLConnect](../content/SQLConnect-Function.md) or [SQLDriverConnect](../content/SQLDriverConnect-Function.md)).  
  
 Whenever a driver returns SQL_SUCCESS_WITH_INFO, the Driver Manager will obtain the diagnostic information from *hDbcInfoToken*, and return SQL_SUCCESS_WITH_INFO to the application in [SQLConnect](../content/SQLConnect-Function.md) and [SQLDriverConnect](../content/SQLDriverConnect-Function.md).  
  
 Applications should not call this function directly. An ODBC driver that supports driver-aware connection pooling must implement this function.  
  
 Include sqlspi.h for ODBC driver development.  
  
## See Also  
 [Developing an ODBC Driver](../content/Developing-an-ODBC-Driver.md)   
 [Driver-Aware Connection Pooling](../content/Driver-Aware-Connection-Pooling.md)   
 [Developing Connection-Pool Awareness in an ODBC Driver](../content/Developing-Connection-Pool-Awareness-in-an-ODBC-Driver.md)