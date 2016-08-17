---
title: "ODBC Functions and the Cursor Library"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c609d0fb-787a-4b39-9673-332d411b3d63
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# ODBC Functions and the Cursor Library
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work and plan to modify applications that currently use this feature. Microsoft recommends using the driver's cursor functionality.  
  
 When the ODBC cursor library is enabled for a connection, the Driver Manager calls functions in the cursor library instead of in the driver. The cursor library either executes the function or calls it in the specified driver.  
  
 This section contains the following topics.  
  
-   [ODBC Functions Executed by the Cursor Library](../content/ODBC-Functions-Executed-by-the-Cursor-Library.md)  
  
-   [ODBC Functions Not Executed by the Cursor Library](../content/ODBC-Functions-Not-Executed-by-the-Cursor-Library.md)  
  
-   [SQLBindCol (Cursor Library)](../content/SQLBindCol--Cursor-Library-.md)  
  
-   [SQLBindParameter (Cursor Library)](../content/SQLBindParameter--Cursor-Library-.md)  
  
-   [SQLBulkOperations (Cursor Library)](../content/SQLBulkOperations-and-the-Cursor-Library.md)  
  
-   [SQLCloseCursor (Cursor Library)](../content/SQLCloseCursor_ODBC.md)  
  
-   [SQLEndTran (Cursor Library)](../content/SQLEndTran--Cursor-Library-.md)  
  
-   [SQLExtendedFetch (Cursor Library)](../content/SQLExtendedFetch--Cursor-Library-.md)  
  
-   [SQLFetch (Cursor Library)](../content/SQLFetch--Cursor-Library-.md)  
  
-   [SQLFetchScroll (Cursor Library)](../content/SQLFetchScroll--Cursor-Library-.md)  
  
-   [SQLFreeStmt (Cursor Library)](../content/SQLFreeStmt--Cursor-Library-.md)  
  
-   [SQLGetData (Cursor Library)](../content/SQLGetData--Cursor-Library-.md)  
  
-   [SQLGetDescField and SQLGetDescRec (Cursor Library)](../content/SQLGetDescField-and-SQLGetDescRec--Cursor-Library-.md)  
  
-   [SQLGetFunctions (Cursor Library)](../content/SQLGetFunctions--Cursor-Library-.md)  
  
-   [SQLGetInfo (Cursor Library)](../content/SQLGetInfo--Cursor-Library-.md)  
  
-   [SQLGetStmtAttr (Cursor Library)](../content/SQLGetStmtAttr--Cursor-Library-.md)  
  
-   [SQLGetStmtOption (Cursor Library)](../content/SQLGetStmtOption--Cursor-Library-.md)  
  
-   [SQLNativeSql (Cursor Library)](../content/SQLNativeSql--Cursor-Library-.md)  
  
-   [SQLRowCount (Cursor Library)](../content/SQLRowCount--Cursor-Library-.md)  
  
-   [SQLSetConnectAttr (Cursor Library)](../content/SQLSetConnectAttr--Cursor-Library-.md)  
  
-   [SQLSetDescField and SQLSetDescRec (Cursor Library)](../content/SQLSetDescField-and-SQLSetDescRec--Cursor-Library-.md)  
  
-   [SQLSetEnvAttr (Cursor Library)](../content/SQLSetEnvAttr-and-the-Cursor-Library.md)  
  
-   [SQLSetPos (Cursor Library)](../content/SQLSetPos--Cursor-Library-.md)  
  
-   [SQLSetScrollOptions (Cursor Library)](../content/SQLSetScrollOptions--Cursor-Library-.md)  
  
-   [SQLSetStmtAttr (Cursor Library)](../content/SQLSetStmtAttr--Cursor-Library-.md)