---
title: "ODBC Function Summary"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7aa635da-e6b7-439f-8e9b-c3860e24de5e
caps.latest.revision: 14
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# ODBC Function Summary
The following table lists ODBC functions, grouped by type of task, and includes the conformance designation and a brief description of the purpose of each function. For more information about conformance designations, see [ODBC and the Standard CLI](../content/ODBC-and-the-Standard-CLI.md). For more information about the syntax and semantics for each function, see [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 An application can call the **SQLGetInfo** function to obtain conformance information about a driver. To obtain information about support for a specific function in a driver, an application can call **SQLGetFunctions**.  
  
|Task|Function name|Conformance|Purpose|  
|----------|-------------------|-----------------|-------------|  
|Connecting to a data source|[SQLAllocHandle](../content/SQLAllocHandle-Function.md)|ISO 92|Obtains an environment, connection, statement, or descriptor handle.|  
||[SQLConnect](../content/SQLConnect-Function.md)|ISO 92|Connects to a specific driver by data source name, user ID, and password.|  
||[SQLDriverConnect](../content/SQLDriverConnect-Function.md)|ODBC|Connects to a specific driver by connection string or requests that the Driver Manager and driver display connection dialog boxes for the user.|  
||[SQLBrowseConnect](../content/SQLBrowseConnect-Function.md)|ODBC|Returns successive levels of connection attributes and valid attribute values. When a value has been specified for each connection attribute, connects to the data source.|  
|Obtaining information about a driver and data source|[SQLDataSources](../content/SQLDataSources-Function.md)<br /><br /> [SQLDrivers](../content/SQLDrivers-Function.md)|ISO 92<br /><br /> ODBC|Returns the list of available data sources.<br /><br /> Returns the list of installed drivers and their attributes.|  
||[SQLGetInfo](../content/SQLGetInfo-Function.md)|ISO 92|Returns information about a specific driver and data source.|  
||[SQLGetFunctions](../content/SQLGetFunctions-Function.md)|ISO 92|Returns supported driver functions.|  
||[SQLGetTypeInfo](../content/SQLGetTypeInfo-Function.md)|ISO 92|Returns information about supported data types.|  
|Setting and retrieving driver attributes|[SQLSetConnectAttr](../content/SQLSetConnectAttr-Function.md)<br /><br /> [SQLGetConnectAttr](../content/SQLGetConnectAttr-Function.md)|ISO 92<br /><br /> ISO 92|Sets a connection attribute.<br /><br /> Returns the value of a connection attribute.|  
||[SQLSetEnvAttr](../content/SQLSetEnvAttr-Function.md)|ISO 92|Sets an environment attribute.|  
||[SQLGetEnvAttr](../content/SQLGetEnvAttr-Function.md)|ISO 92|Returns the value of an environment attribute.|  
||[SQLSetStmtAttr](../content/SQLSetStmtAttr-Function.md)|ISO 92|Sets a statement attribute.|  
||[SQLGetStmtAttr](../content/SQLGetStmtAttr-Function.md)|ISO 92|Returns the value of a statement attribute.|  
|Setting and retrieving descriptor fields|[SQLGetDescField](../content/SQLGetDescField-Function.md)<br /><br /> [SQLGetDescRec](../content/SQLGetDescRec-Function.md)|ISO 92<br /><br /> ISO 92|Returns the value of a single descriptor field.<br /><br /> Returns the values of multiple descriptor fields.|  
||[SQLSetDescField](../content/SQLSetDescField-Function.md)|ISO 92|Sets a single descriptor field.|  
||[SQLSetDescRec](../content/SQLSetDescRec-Function.md)|ISO 92|Sets multiple descriptor fields.|  
||[SQLCopyDesc](../content/SQLCopyDesc-Function.md)|ISO 92|Copies descriptor information from one descriptor handle to another.|  
|Preparing SQL requests|[SQLPrepare](../content/SQLPrepare-Function.md)|ISO 92|Prepares an SQL statement for later execution.|  
||[SQLBindParameter](../content/SQLBindParameter-Function.md)|ODBC|Assigns storage for a parameter in an SQL statement.|  
||[SQLGetCursorName](../content/SQLGetCursorName-Function.md)|ISO 92|Returns the cursor name associated with a statement handle.|  
||[SQLSetCursorName](../content/SQLSetCursorName-Function.md)|ISO 92|Specifies a cursor name.|  
||[SQLSetScrollOptions](../content/SQLSetScrollOptions-Function.md)|ODBC|Sets options that control cursor behavior.|  
|Submitting requests|[SQLExecute](../content/SQLExecute-Function.md)<br /><br /> [SQLExecDirect](../content/SQLExecDirect-Function.md)|ISO 92<br /><br /> ISO 92|Executes a prepared statement.<br /><br /> Executes a statement.|  
||[SQLNativeSql](../content/SQLNativeSql-Function.md)|ODBC|Returns the text of an SQL statement as translated by the driver.|  
||[SQLDescribeParam](../content/SQLDescribeParam-Function.md)|ODBC|Returns the description for a specific parameter in a statement.|  
||[SQLNumParams](../content/SQLNumParams-Function.md)|ISO 92|Returns the number of parameters in a statement.|  
||[SQLParamData](../content/SQLParamData-Function.md)|ISO 92|Used in conjunction with **SQLPutData** to supply parameter data at execution time. (Useful for long data values.)|  
||[SQLPutData](../content/SQLPutData-Function.md)|ISO 92|Sends part or all of a data value for a parameter. (Useful for long data values.)|  
|Retrieving results and information about results|[SQLRowCount](../content/SQLRowCount-Function.md)<br /><br /> [SQLNumResultCols](../content/SQLNumResultCols-Function.md)|ISO 92<br /><br /> ISO 92|Returns the number of rows affected by an insert, update, or delete request.<br /><br /> Returns the number of columns in the result set.|  
||[SQLDescribeCol](../content/SQLDescribeCol-Function.md)|ISO 92|Describes a column in the result set.|  
||[SQLColAttribute](../content/SQLColAttribute-Function.md)|ISO 92|Describes attributes of a column in the result set.|  
||[SQLBindCol](../content/SQLBindCol-Function.md)|ISO 92|Assigns storage for a result column and specifies the data type.|  
||[SQLFetch](../content/SQLFetch-Function.md)|ISO 92|Returns multiple result rows.|  
||[SQLFetchScroll](../content/SQLFetchScroll-Function.md)|ISO 92|Returns scrollable result rows.|  
||[SQLGetData](../content/SQLGetData-Function.md)|ISO 92|Returns part or all of one column of one row of a result set. (Useful for long data values.)|  
||[SQLSetPos](../content/SQLSetPos-Function.md)|ODBC|Positions a cursor within a fetched block of data and allows an application to refresh data in the rowset or to update or delete data in the result set.|  
||[SQLBulkOperations](../content/SQLBulkOperations-Function.md)|ODBC|Performs bulk insertions and bulk bookmark operations, including update, delete, and fetch by bookmark.|  
||[SQLMoreResults](../content/SQLMoreResults-Function.md)|ODBC|Determines whether there are more result sets available and, if so, initializes processing for the next result set.|  
||[SQLGetDiagField](../content/SQLGetDiagField-Function.md)|ISO 92|Returns additional diagnostic information (a single field of the diagnostic data structure).|  
||[SQLGetDiagRec](../content/SQLGetDiagRec-Function.md)|ISO 92|Returns additional diagnostic information (multiple fields of the diagnostic data structure).|  
|Obtaining information about the data source's system tables (catalog functions)|[SQLColumnPrivileges](../content/SQLColumnPrivileges-Function.md)<br /><br /> [SQLColumns](../content/SQLColumns-Function.md)|ODBC<br /><br /> Open Group|Returns a list of columns and associated privileges for one or more tables.<br /><br /> Returns the list of column names in specified tables.|  
||[SQLForeignKeys](../content/SQLForeignKeys-Function.md)|ODBC|Returns a list of column names that make up foreign keys, if they exist for a specified table.|  
||[SQLPrimaryKeys](../content/SQLPrimaryKeys-Function.md)|ODBC|Returns the list of column names that make up the primary key for a table.|  
||[SQLProcedureColumns](../content/SQLProcedureColumns-Function.md)|ODBC|Returns the list of input and output parameters, as well as the columns that make up the result set for the specified procedures.|  
||[SQLProcedures](../content/SQLProcedures-Function.md)|ODBC|Returns the list of procedure names stored in a specific data source.|  
||[SQLSpecialColumns](../content/SQLSpecialColumns-Function.md)|Open Group|Returns information about the optimal set of columns that uniquely identifies a row in a specified table, or the columns that are automatically updated when any value in the row is updated by a transaction.|  
||[SQLStatistics](../content/SQLStatistics-Function.md)|ISO 92|Returns statistics about a single table and the list of indexes associated with the table.|  
||[SQLTablePrivileges](../content/SQLTablePrivileges-Function.md)|ODBC|Returns a list of tables and the privileges associated with each table.|  
||[SQLTables](../content/SQLTables-Function.md)|Open Group|Returns the list of table names stored in a specific data source.|  
|Terminating a statement|[SQLFreeStmt](../content/SQLFreeStmt-Function.md)|ISO 92|Ends statement processing, discards pending results, and, optionally, frees all resources associated with the statement handle.|  
||[SQLCloseCursor](../content/SQLCloseCursor-Function.md)|ISO 92|Closes a cursor that has been opened on a statement handle.|  
||[SQLCancel](../content/SQLCancel-Function.md)|ISO 92|Cancels the processing on a statement.|  
||[SQLCancelHandle](../content/SQLCancelHandle-Function.md)|ODBC|Cancels the processing on a statement or connection.|  
||[SQLEndTran](../content/SQLEndTran-Function.md)|ISO 92|Commits or rolls back a transaction.|  
|Terminating a connection|[SQLDisconnect](../content/SQLDisconnect-Function.md)<br /><br /> [SQLFreeHandle](../content/SQLFreeHandle-Function.md)|ISO 92<br /><br /> ISO 92|Closes the connection.<br /><br /> Releases an environment, connection, statement, or descriptor handle.|