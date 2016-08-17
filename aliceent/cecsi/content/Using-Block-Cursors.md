---
title: "Using Block Cursors"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2aad7d6b-216e-47e7-b3cb-f95ad096f21a
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Using Block Cursors
Support for block cursors is built into ODBC 3.*x*. **SQLFetch** can be used only for multirow fetches when called in ODBC 3.*x*; if an ODBC 2.*x* application calls **SQLFetch**, it will open only a single-row, forward-only cursor. When an ODBC 3.*x* application calls **SQLFetch** in an ODBC 2.*x* driver, it returns a single row unless the driver supports **SQLExtendedFetch**. For more information, see [Block Cursors, Scrollable Cursors, and Backward Compatibility](../content/Block-Cursors--Scrollable-Cursors--and-Backward-Compatibility.md) in Appendix G: Driver Guidelines for Backward Compatibility.  
  
 To use block cursors, the application sets the rowset size, binds the rowset buffers (as described in the previous section), optionally sets the SQL_ATTR_ROWS_FETCHED_PTR and SQL_ATTR_ROW_STATUS_PTR statement attributes, and calls **SQLFetch** or **SQLFetchScroll** to fetch a block of rows. The application can change the rowset size and bind new rowset buffers (by calling **SQLBindCol** or specifying a bind offset) even after rows have been fetched.  
  
 This section contains the following topics.  
  
-   [Rowset Size](../content/Rowset-Size.md)  
  
-   [Number of Rows Fetched and Status](../content/Number-of-Rows-Fetched-and-Status.md)  
  
-   [SQLGetData and Block Cursors; block curso](../content/SQLGetData-and-Block-Cursors.md)