---
title: "Mapping Deprecated Functions"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ee462617-1d79-4c88-afeb-b129cff34cc6
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Mapping Deprecated Functions
This section describes how deprecated functions are mapped by the ODBC 3*.x* Driver Manager to guarantee backward compatibility of ODBC 3*.x* drivers that are used with ODBC 2.*x* applications. The Driver Manager performs this mapping regardless of the version of the application. Because each of the ODBC 2.*x* functions in the following list is mapped to the corresponding ODBC 3*.x* function when called in an ODBC 3*.x* driver, the ODBC 3*.x* driver does not have to implement the ODBC 2.*x* functions.  
  
 The mapping in the list is triggered when the driver is an ODBC 3*.x* driver and the driver does not support the function that is being mapped.  
  
 The following table lists all duplicated functionality that was introduced in ODBC 3*.x*.  
  
|ODBC 2.*x* function|ODBC 3*.x* function|  
|-------------------------|-------------------------|  
|**SQLAllocConnect**|**SQLAllocHandle**|  
|**SQLAllocEnv**|**SQLAllocHandle**|  
|**SQLAllocStmt**|**SQLAllocHandle**|  
|**SQLBindParam**[1]|**SQLBindParameter**|  
|**SQLColAttributes**|**SQLColAttribute**|  
|**SQLError**|**SQLGetDiagRec**|  
|**SQLFreeConnect**|**SQLFreeHandle**|  
|**SQLFreeEnv**|**SQLFreeHandle**|  
|**SQLFreeStmt** with an *Option* of SQL_DROP|**SQLFreeHandle**|  
|**SQLGetConnectOption**|**SQLGetConnectAttr**|  
|**SQLGetStmtOption**|**SQLGetStmtAttr**|  
|**SQLParamOptions**|**SQLSetStmtAttr**|  
|**SQLSetConnectOption**|**SQLSetConnectAttr**|  
|**SQLSetParam**[2]|**SQLBindParameter**|  
|**SQLSetScrollOption**|**SQLSetStmtAttr**|  
|**SQLSetStmtOption**|**SQLSetStmtAttr**|  
|**SQLTransact**|**SQLEndTran**|  
  
 [1]   Even though this function did not exist in ODBC 2*.x*, it is in the Open Group and ISO standards.  
  
 [2]   This is an ODBC 1.0 function.  
  
 This section contains the following topics.  
  
-   [SQLAllocConnect Mapping](../content/SQLAllocConnect-Mapping.md)  
  
-   [SQLAllocEnv Mapping](../content/SQLAllocEnv-Mapping.md)  
  
-   [SQLAllocStmt Mapping](../content/SQLAllocStmt-Mapping.md)  
  
-   [SQLBindParam Mapping](../content/SQLBindParam-Mapping.md)  
  
-   [SQLColAttributes Mapping](../content/SQLColAttributes-Mapping.md)  
  
-   [SQLError Mapping](../content/SQLError-Mapping.md)  
  
-   [SQLFreeConnect Mapping](../content/SQLFreeConnect-Mapping.md)  
  
-   [SQLFreeEnv Mapping](../content/SQLFreeEnv-Mapping.md)  
  
-   [SQLFreeStmt Mapping](../content/SQLFreeStmt-Mapping.md)  
  
-   [SQLGetConnectOption Mapping](../content/SQLGetConnectOption-Mapping.md)  
  
-   [SQLGetStmtOption Mapping](../content/SQLGetStmtOption-Mapping.md)  
  
-   [SQLInstallTranslator Mapping](../content/SQLInstallTranslator-Mapping.md)  
  
-   [SQLParamOptions Mapping](../content/SQLParamOptions-Mapping.md)  
  
-   [SQLSetConnectOption Mapping](../content/SQLSetConnectOption-Mapping.md)  
  
-   [SQLSetParam Mapping](../content/SQLSetParam-Mapping.md)  
  
-   [SQLSetScrollOptions Mapping](../content/SQLSetScrollOptions-Mapping.md)  
  
-   [SQLSetStmtOption Mapping](../content/SQLSetStmtOption-Mapping.md)  
  
-   [SQLTransact Mapping](../content/SQLTransact-Mapping.md)