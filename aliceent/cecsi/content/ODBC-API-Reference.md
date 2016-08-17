---
title: "ODBC API Reference"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apitype: dllExport
ms.assetid: b7a49774-f458-44ce-9a04-a0457501405b
caps.latest.revision: 10
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# ODBC API Reference
The topics in this section describe each ODBC function in alphabetical order. Each function is defined as a C programming language function. Descriptions include the following:  
  
-   Purpose  
  
-   ODBC version  
  
-   Standard CLI conformance level  
  
-   Syntax  
  
-   Arguments  
  
-   Return values  
  
-   Diagnostics  
  
-   Comments about usage and implementation  
  
-   Code example  
  
-   References to related functions  
  
 The standard CLI conformance level can be one of the following: ISO 92, Open Group, ODBC, or Deprecated. A function tagged as ISO 92–conformant also appears in Open Group version 1, because Open Group is a pure superset of ISO 92. A function tagged as Open Group-compliant also appears in ODBC 3.*x*, because ODBC 3.*x* is a pure superset of Open Group version 1. A function tagged as ODBC-compliant appears in neither standard. A function tagged as deprecated has been deprecated in ODBC 3.*x*.  
  
 Handling of diagnostic information is described in the [SQLGetDiagField](../content/SQLGetDiagField-Function.md) function description. The text associated with SQLSTATE values is included to provide a description of the condition but is not intended to prescribe specific text.  
  
> [!NOTE]  
>  For driver-specific information about ODBC functions, see the section for the driver.  
  
 This section contains topics for the following functions:  
  
-   [SQLAllocConnect Function](../content/SQLAllocConnect-Function.md)  
  
-   [SQLAllocEnv Function](../content/SQLAllocEnv-Function.md)  
  
-   [SQLAllocHandle Function](../content/SQLAllocHandle-Function.md)  
  
-   [SQLAllocStmt Function](../content/SQLAllocStmt-Function.md)  
  
-   [SQLBindCol Function](../content/SQLBindCol-Function.md)  
  
-   [SQLBindParameter Function](../content/SQLBindParameter-Function.md)  
  
-   [SQLBrowseConnect Function](../content/SQLBrowseConnect-Function.md)  
  
-   [SQLBulkOperations Function](../content/SQLBulkOperations-Function.md)  
  
-   [SQLCancel Function](../content/SQLCancel-Function.md)  
  
-   [SQLCancelHandle Function](../content/SQLCancelHandle-Function.md)  
  
-   [SQLCloseCursor Function](../content/SQLCloseCursor-Function.md)  
  
-   [SQLColAttribute Function](../content/SQLColAttribute-Function.md)  
  
-   [SQLColAttributes Function](../content/SQLColAttributes-Function.md)  
  
-   [SQLColumnPrivileges Function](../content/SQLColumnPrivileges-Function.md)  
  
-   [SQLColumns Function](../content/SQLColumns-Function.md)  
  
-   [SQLCompleteAsync Function](../content/SQLCompleteAsync-Function.md)  
  
-   [SQLConnect Function](../content/SQLConnect-Function.md)  
  
-   [SQLCopyDesc Function](../content/SQLCopyDesc-Function.md)  
  
-   [SQLDataSources Function](../content/SQLDataSources-Function.md)  
  
-   [SQLDescribeCol Function](../content/SQLDescribeCol-Function.md)  
  
-   [SQLDescribeParam Function](../content/SQLDescribeParam-Function.md)  
  
-   [SQLDisconnect Function](../content/SQLDisconnect-Function.md)  
  
-   [SQLDriverConnect Function](../content/SQLDriverConnect-Function.md)  
  
-   [SQLDrivers Function](../content/SQLDrivers-Function.md)  
  
-   [SQLEndTran Function](../content/SQLEndTran-Function.md)  
  
-   [SQLError Function](../content/SQLError-Function.md)  
  
-   [SQLExecDirect Function](../content/SQLExecDirect-Function.md)  
  
-   [SQLExecute Function](../content/SQLExecute-Function.md)  
  
-   [SQLExtendedFetch Function](../content/SQLExtendedFetch-Function.md)  
  
-   [SQLFetch Function](../content/SQLFetch-Function.md)  
  
-   [SQLFetchScroll Function](../content/SQLFetchScroll-Function.md)  
  
-   [SQLForeignKeys Function](../content/SQLForeignKeys-Function.md)  
  
-   [SQLFreeConnect Function](../content/SQLFreeConnect-Function.md)  
  
-   [SQLFreeEnv Function](../content/SQLFreeEnv-Function.md)  
  
-   [SQLFreeHandle Function](../content/SQLFreeHandle-Function.md)  
  
-   [SQLFreeStmt Function](../content/SQLFreeStmt-Function.md)  
  
-   [SQLGetConnectAttr Function](../content/SQLGetConnectAttr-Function.md)  
  
-   [SQLGetConnectOption Function](../content/SQLGetConnectOption-Function.md)  
  
-   [SQLGetCursorName Function](../content/SQLGetCursorName-Function.md)  
  
-   [SQLGetData Function](../content/SQLGetData-Function.md)  
  
-   [SQLGetDescField Function](../content/SQLGetDescField-Function.md)  
  
-   [SQLGetDescRec Function](../content/SQLGetDescRec-Function.md)  
  
-   [SQLGetDiagField Function](../content/SQLGetDiagField-Function.md)  
  
-   [SQLGetDiagRec Function](../content/SQLGetDiagRec-Function.md)  
  
-   [SQLGetEnvAttr Function](../content/SQLGetEnvAttr-Function.md)  
  
-   [SQLGetFunctions Function](../content/SQLGetFunctions-Function.md)  
  
-   [SQLGetInfo Function](../content/SQLGetInfo-Function.md)  
  
-   [SQLGetStmtAttr Function](../content/SQLGetStmtAttr-Function.md)  
  
-   [SQLGetStmtOption Function](../content/SQLGetStmtOption-Function.md)  
  
-   [SQLGetTypeInfo Function](../content/SQLGetTypeInfo-Function.md)  
  
-   [SQLMoreResults Function](../content/SQLMoreResults-Function.md)  
  
-   [SQLNativeSql Function](../content/SQLNativeSql-Function.md)  
  
-   [SQLNumParams Function](../content/SQLNumParams-Function.md)  
  
-   [SQLNumResultCols Function](../content/SQLNumResultCols-Function.md)  
  
-   [SQLParamData Function](../content/SQLParamData-Function.md)  
  
-   [SQLParamOptions Function](../content/SQLParamOptions-Function.md)  
  
-   [SQLPrepare Function](../content/SQLPrepare-Function.md)  
  
-   [SQLPrimaryKeys Function](../content/SQLPrimaryKeys-Function.md)  
  
-   [SQLProcedureColumns Function](../content/SQLProcedureColumns-Function.md)  
  
-   [SQLProcedures Function](../content/SQLProcedures-Function.md)  
  
-   [SQLPutData Function](../content/SQLPutData-Function.md)  
  
-   [SQLRowCount Function](../content/SQLRowCount-Function.md)  
  
-   [SQLSetConnectAttr Function](../content/SQLSetConnectAttr-Function.md)  
  
-   [SQLSetConnectOption Function](../content/SQLSetConnectOption-Function.md)  
  
-   [SQLSetCursorName Function](../content/SQLSetCursorName-Function.md)  
  
-   [SQLSetDescField Function](../content/SQLSetDescField-Function.md)  
  
-   [SQLSetDescRec Function](../content/SQLSetDescRec-Function.md)  
  
-   [SQLSetEnvAttr Function](../content/SQLSetEnvAttr-Function.md)  
  
-   [SQLSetParam Function](../content/SQLSetParam-Function.md)  
  
-   [SQLSetPos Function](../content/SQLSetPos-Function.md)  
  
-   [SQLSetScrollOptions Function](../content/SQLSetScrollOptions-Function.md)  
  
-   [SQLSetStmtAttr Function](../content/SQLSetStmtAttr-Function.md)  
  
-   [SQLSetStmtOption Function](../content/SQLSetStmtOption-Function.md)  
  
-   [SQLSpecialColumns Function](../content/SQLSpecialColumns-Function.md)  
  
-   [SQLStatistics Function](../content/SQLStatistics-Function.md)  
  
-   [SQLTablePrivileges Function](../content/SQLTablePrivileges-Function.md)  
  
-   [SQLTables Function](../content/SQLTables-Function.md)  
  
-   [SQLTransact Function](../content/SQLTransact-Function.md)