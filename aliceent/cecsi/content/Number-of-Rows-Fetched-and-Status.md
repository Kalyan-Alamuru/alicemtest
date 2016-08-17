---
title: "Number of Rows Fetched and Status"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a069b979-5108-4905-932f-8ae8e7905ff2
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Number of Rows Fetched and Status
If the SQL_ATTR_ROWS_FETCHED_PTR statement attribute has been set, it specifies a buffer that returns the number of rows fetched by the call to **SQLFetch** or **SQLFetchScroll**, and error rows. (This number is a count of all rows that do not have the status SQL_ROW_NO_ROWS.) After a call to **SQLBulkOperations** or **SQLSetPos**, the buffer contains the number of rows that were affected by a bulk operation performed by the function. If the SQL_ATTR_ROW_STATUS_PTR statement attribute has been set, **SQLFetch** or **SQLFetchScroll** returns the *row status array,* which provides the status of each returned row. Both of the buffers pointed to by these fields are allocated by the application and populated by the driver. An application must make sure that these pointers remain valid until the cursor is closed.  
  
 Entries in the row status array state whether each row was fetched successfully, whether it was updated, added, or deleted since it was last fetched, and whether an error occurred while fetching the row. If **SQLFetch** or **SQLFetchScroll** encounters an error while retrieving one row of a multirow rowset, or if **SQLBulkOperations** with an *Operation* argument of SQL_FETCH_BY_BOOKMARK encounters an error while performing a bulk fetch, it sets the corresponding value in the row status array to SQL_ROW_ERROR, continues fetching rows, and returns SQL_SUCCESS_WITH_INFO. For more information about error handling and the row status array, see the [SQLFetch](../content/SQLFetch-Function.md) and [SQLFetchScroll](../content/SQLFetchScroll-Function.md) function descriptions.