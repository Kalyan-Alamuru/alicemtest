---
title: "Retrieving Bookmarks"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a34c8f09-b786-4835-a44b-b7294c970aff
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Retrieving Bookmarks
If the application will use bookmarks, it must set the SQL_ATTR_USE_BOOKMARKS statement attribute to SQL_UB_VARIABLE before preparing or executing the statement. This is necessary because building and maintaining bookmarks can be an expensive operation, so bookmarks should be enabled only when an application can make good use of them.  
  
 Bookmarks are returned as column 0 of the result set. There are three ways an application can retrieve them:  
  
-   Bind column 0 of the result set. **SQLFetch** or **SQLFetchScroll** returns the bookmarks for each row in the rowset along with the data for other bound columns.  
  
-   Call **SQLSetPos** to position to a row in the rowset and then call **SQLGetData** for column 0. If a driver supports bookmarks, it must always support the ability to call **SQLGetData** for column 0, even if it does not allow applications to call **SQLGetData** for other columns before the last bound column.  
  
-   Call **SQLBulkOperations** with the *Operation* argument set to SQL_ADD, and column 0 bound. The cursor inserts the row and returns the bookmark for the row in the bound buffer.