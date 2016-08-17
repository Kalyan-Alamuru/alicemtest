---
title: "ODBC Functions and the Visual FoxPro ODBC Driver"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 512f9cee-ffad-439b-b612-b49c34c32658
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# ODBC Functions and the Visual FoxPro ODBC Driver
The topics in this section provide a brief summary of ODBC API functions and any Visual FoxPro–specific details.  
  
> [!NOTE]  
>  For general information about ODBC functions, see [ODBC API Reference](../content/ODBC-API-Reference.md) in "ODBC Programmer's Guide".  
  
 The ODBC API functions have been divided into three main categories here: Core Level API functions, Level 1 API functions, and Level 2 API functions.  
  
> [!NOTE]  
>  Several of the functions behave differently depending on whether the data source is defined as a connection to a directory of [free tables](../content/Visual-FoxPro-Terminology.md) (.dbf files) or to a Visual FoxPro [database](../content/Visual-FoxPro-Terminology.md) (.dbc file). Certain operations are supported only for database connections.  
  
## Core Level API Support  
 The ODBC Core Level API functions are listed in the following table. All of these functions are supported by the Visual FoxPro ODBC Driver.  
  
|||  
|-|-|  
|[SQLAllocConnect](../content/SQLAllocConnect--Visual-FoxPro-ODBC-Driver-.md)|[SQLExecute](../content/SQLExecute--Visual-FoxPro-ODBC-Driver-.md)|  
|[SQLAllocEnv](../content/SQLAllocEnv--Visual-FoxPro-ODBC-Driver-.md)|[SQLFetch](../content/SQLFetch--Visual-FoxPro-ODBC-Driver-.md)|  
|[SQLAllocStmt](../content/SQLAllocStmt--Visual-FoxPro-ODBC-Driver-.md)|[SQLFreeConnect](../content/SQLFreeConnect--Visual-FoxPro-ODBC-Driver-.md)|  
|[SQLBindCol](../content/SQLBindCol--Visual-FoxPro-ODBC-Driver-.md)|[SQLFreeEnv](../content/SQLFreeEnv--Visual-FoxPro-ODBC-Driver-.md)|  
|[SQLCancel](../content/SQLCancel--Visual-FoxPro-ODBC-Driver-.md)|[SQLFreeStmt](../content/SQLFreeStmt--Visual-FoxPro-ODBC-Driver-.md)|  
|[SQLColAttributes](../content/SQLColAttributes--Visual-FoxPro-ODBC-Driver-.md)|[SQLGetCursorName](../content/SQLGetCursorName--Visual-FoxPro-ODBC-Driver-.md)|  
|[SQLConnect](../content/SQLConnect--Visual-FoxPro-ODBC-Driver-.md)|[SQLNumResultCols](../content/SQLNumResultCols--Visual-FoxPro-ODBC-Driver-.md)|  
|[SQLDescribeCol](../content/SQLDescribeCol--Visual-FoxPro-ODBC-Driver-.md)|[SQLPrepare](../content/SQLPrepare--Visual-FoxPro-ODBC-Driver-.md)|  
|[SQLDisconnect](../content/SQLDisconnect--Visual-FoxPro-ODBC-Driver-.md)|[SQLRowCount](../content/SQL-Row-Count--Visual-FoxPro-ODBC-Driver-.md)|  
|[SQLError](../content/SQLError--Visual-FoxPro-ODBC-Driver-.md)|[SQLSetCursorName](../content/SQLSetCursorName--Visual-FoxPro-ODBC-Driver-.md)|  
|[SQLExecDirect](../content/SQLExecDirect--Visual-FoxPro-ODBC-Driver-.md)|[SQLTransact](../content/SQLTransact--Visual-FoxPro-ODBC-Driver-.md)|  
  
## Level 1 API Support  
 The ODBC Level 1 API functions are listed in the following table. All of these functions are fully or partially supported by the Visual FoxPro ODBC Driver.  
  
|||  
|-|-|  
|[SQLBindParameter](../content/SQLBindParameter--Visual-FoxPro-ODBC-Driver-.md)|[SQLGetTypeInfo](../content/SQLGetTypeInfo--Visual-FoxPro-ODBC-Driver-.md)|  
|[SQLColumns](../content/SQLColumns--Visual-FoxPro-ODBC-Driver-.md)|[SQLParamData](../content/SQLParamData--Visual-FoxPro-ODBC-Driver-.md)|  
|[SQLDriverConnect](../content/SQLDriverConnect--Visual-FoxPro-ODBC-Driver-.md)|[SQLPutData](../content/SQLPutData--Visual-FoxPro-ODBC-Driver-.md)|  
|[SQLGetConnectOption](../content/SQLGetConnectOption--Visual-FoxPro-ODBC-Driver-.md)|[SQLSetConnectOption](../content/SQLSetConnectOption--Visual-FoxPro-ODBC-Driver-.md)|  
|[SQLGetData](../content/SQLGetData--Visual-FoxPro-ODBC-Driver-.md)|[SQLSetStmtOption](../content/SQLSetStmtOption--Visual-FoxPro-ODBC-Driver-.md)|  
|[SQLGetFunctions](../content/SQLGetFunctions--Visual-FoxPro-ODBC-Driver-.md)|[SQLSpecialColumns](../content/SQLSpecialColumns--Visual-FoxPro-ODBC-Driver-.md)|  
|[SQLGetInfo](../content/SQLGetInfo--Visual-FoxPro-ODBC-Driver-.md)|[SQLStatistics](../content/SQLStatistics--Visual-FoxPro-ODBC-Driver-.md)|  
|[SQLGetStmtOption](../content/SQLGetStmtOption--Visual-FoxPro-ODBC-Driver-.md)|[SQLTables](../content/SQLTables--Visual-FoxPro-ODBC-Driver-.md)|  
  
## Level 2 API Support  
 The following ODBC Level 2 API functions are fully or partially supported:  
  
-   [SQLDataSources](../content/SQLDataSources--Visual-FoxPro-ODBC-Driver-.md)  
  
-   [SQLDrivers](../content/SQLDrivers--Visual-FoxPro-ODBC-Driver-.md)  
  
-   [SQLExtendedFetch](../content/SQLExtendedFetch--Visual-FoxPro-ODBC-Driver-.md)  
  
-   [SQLMoreResults](../content/SQLMoreResults--Visual-FoxPro-ODBC-Driver-.md)  
  
-   [SQLNumParams](../content/SQLNumParams--Visual-FoxPro-ODBC-Driver-.md)  
  
-   [SQLParamOptions](../content/SQLParamOptions--Visual-FoxPro-ODBC-Driver-.md)  
  
-   [SQLPrimaryKeys](../content/SQLPrimaryKeys--Visual-FoxPro-ODBC-Driver-.md)  
  
-   [SQLSetPos](../content/SQLSetPos--Visual-FoxPro-ODBC-Driver-.md)  
  
-   [SQLSetScrollOptions](../content/SQLSetScrollOptions--Visual-FoxPro-ODBC-Driver-.md) (partial support)  
  
 The following Level 2 API functions are not supported:  
  
-   SQLBrowseConnect  
  
-   SQLColumnPrivileges  
  
-   SQLDescribeParam  
  
-   SQLForeignKeys  
  
-   SQLNativeSql  
  
-   SQLProcedureColumns  
  
-   SQLProcedures  
  
-   SQLTablePrivileges