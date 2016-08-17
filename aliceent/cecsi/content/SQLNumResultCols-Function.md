---
title: "SQLNumResultCols Function"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLNumResultCols
apilocation: 
  - sqlsrv32.dll
apitype: dllExport
ms.assetid: d863179f-12a9-4b55-ac6b-7d84202d3da3
caps.latest.revision: 22
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLNumResultCols Function
**Conformance**  
 Version Introduced: ODBC 1.0 Standards Compliance: ISO 92  
  
 **Summary**  
 **SQLNumResultCols** returns the number of columns in a result set.  
  
## Syntax  
  
```  
  
SQLRETURN SQLNumResultCols(  
     SQLHSTMT        StatementHandle,  
     SQLSMALLINT *   ColumnCountPtr);  
```  
  
## Arguments  
 *StatementHandle*  
 [Input] Statement handle.  
  
 *ColumnCountPtr*  
 [Output] Pointer to a buffer in which to return the number of columns in the result set. This count does not include a bound bookmark column.  
  
## Returns  
 SQL_SUCCESS, SQL_SUCCESS_WITH_INFO, SQL_STILL_EXECUTING, SQL_ERROR, or SQL_INVALID_HANDLE.  
  
## Diagnostics  
 When **SQLNumResultCols** returns SQL_ERROR or SQL_SUCCESS_WITH_INFO, an associated SQLSTATE value can be obtained by calling **SQLGetDiagRec** with a *HandleType* of SQL_HANDLE_STMT and a *Handle* of *StatementHandle*. The following table lists the SQLSTATE values commonly returned by **SQLNumResultCols** and explains each one in the context of this function; the notation "(DM)" precedes the descriptions of SQLSTATEs returned by the Driver Manager. The return code associated with each SQLSTATE value is SQL_ERROR, unless noted otherwise.  
  
|SQLSTATE|Error|Description|  
|--------------|-----------|-----------------|  
|01000|General warning|Driver-specific informational message. (Function returns SQL_SUCCESS_WITH_INFO.)|  
|08S01|Communication link failure|The communication link between the driver and the data source to which the driver was connected failed before the function completed processing.|  
|HY000|General error|An error occurred for which there was no specific SQLSTATE and for which no implementation-specific SQLSTATE was defined. The error message returned by **SQLGetDiagRec** in the *\*MessageText* buffer describes the error and its cause.|  
|HY001|Memory allocation error|The driver was unable to allocate memory required to support execution or completion of the function.|  
|HY008|Operation canceled|Asynchronous processing was enabled for the *StatementHandle*. The function was called, and before it completed execution, **SQLCancel** or **SQLCancelHandle** was called on the *StatementHandle*; the function was then called again on the *StatementHandle*.<br /><br /> The function was called, and before it completed execution, **SQLCancel** or **SQLCancelHandle** was called on the *StatementHandle* from a different thread in a multithread application.|  
|HY010|Function sequence error|(DM) An asynchronously executing function was called for the connection handle that is associated with the *StatementHandle*. This asynchronous function was still executing when the **SQLNumResultsCols** function was called.<br /><br /> (DM) **SQLExecute**, **SQLExecDirect**, or **SQLMoreResults** was called for the *StatementHandle* and returned SQL_PARAM_DATA_AVAILABLE. This function was called before data was retrieved for all streamed parameters.<br /><br /> (DM) The function was called prior to calling **SQLPrepare** or **SQLExecDirect** for the *StatementHandle*.<br /><br /> (DM) An asynchronously executing function (not this one) was called for the *StatementHandle* and was still executing when this function was called.<br /><br /> (DM) **SQLExecute**, **SQLExecDirect**, **SQLBulkOperations**, or **SQLSetPos** was called for the *StatementHandle* and returned SQL_NEED_DATA. This function was called before data was sent for all data-at-execution parameters or columns.<br /><br /> See [SQLPrepare Function](../content/SQLPrepare-Function.md) for details on when a statement handle can be freed.|  
|HY013|Memory management error|The function call could not be processed because the underlying memory objects could not be accessed, possibly because of low memory conditions.|  
|HY117|Connection is suspended due to unknown transaction state. Only disconnect and read-only functions are allowed.|(DM) For more information about suspended state, see [SQLEndTran Function](../content/SQLEndTran-Function.md).|  
|HYT01|Connection timeout expired|The connection timeout period expired before the data source responded to the request. The connection timeout period is set through **SQLSetConnectAttr**, SQL_ATTR_CONNECTION_TIMEOUT.|  
|IM001|Driver does not support this function|(DM) The driver associated with the *StatementHandle* does not support the function.|  
|IM017|Polling is disabled in asynchronous notification mode|Whenever the notification model is used, polling is disabled.|  
|IM018|**SQLCompleteAsync** has not been called to complete the previous asynchronous operation on this handle.|If the previous function call on the handle returns SQL_STILL_EXECUTING and if notification mode is enabled, **SQLCompleteAsync** must be called on the handle to do post-processing and complete the operation.|  
  
 **SQLNumResultCols** can return any SQLSTATE that can be returned by **SQLPrepare** or **SQLExecute** when called after **SQLPrepare** and before **SQLExecute**, depending on when the data source evaluates the SQL statement associated with the statement.  
  
## Comments  
 **SQLNumResultCols** can be called successfully only when the statement is in the prepared, executed, or positioned state.  
  
 If the statement associated with *StatementHandle* does not return columns, **SQLNumResultCols** sets **ColumnCountPtr* to 0.  
  
 The number of columns returned by **SQLNumResultCols** is the same value as the SQL_DESC_COUNT field of the IRD.  
  
 For more information, see [Was a Result Set Created?](../content/Was-a-Result-Set-Created-.md) and [How is Metadata Used?](../content/How-is-Metadata-Used-.md).  
  
## Related Functions  
  
|For information about|See|  
|---------------------------|---------|  
|Binding a buffer to a column in a result set|[SQLBindCol Function](../content/SQLBindCol-Function.md)|  
|Canceling statement processing|[SQLCancel Function](../content/SQLCancel-Function.md)|  
|Returning information about a column in a result set|[SQLColAttribute Function](../content/SQLColAttribute-Function.md)|  
|Returning information about a column in a result set|[SQLDescribeCol Function](../content/SQLDescribeCol-Function.md)|  
|Executing an SQL statement|[SQLExecDirect Function](../content/SQLExecDirect-Function.md)|  
|Executing a prepared SQL statement|[SQLExecute Function](../content/SQLExecute-Function.md)|  
|Fetching a block of data or scrolling through a result set|[SQLFetchScroll Function](../content/SQLFetchScroll-Function.md)|  
|Fetching a single row or a block of data in a forward-only direction|[SQLFetch Function](../content/SQLFetch-Function.md)|  
|Fetching part or all of a column of data|[SQLGetData Function](../content/SQLGetData-Function.md)|  
|Preparing an SQL statement for execution|[SQLPrepare Function](../content/SQLPrepare-Function.md)|  
|Setting cursor scrolling options|[SQLSetStmtAttr Function](../content/SQLSetStmtAttr-Function.md)|  
  
## See Also  
 [ODBC API Reference](../content/ODBC-API-Reference.md)   
 [ODBC Header Files](../content/ODBC-Header-Files.md)