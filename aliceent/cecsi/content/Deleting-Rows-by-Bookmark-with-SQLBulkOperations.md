---
title: "Deleting Rows by Bookmark with SQLBulkOperations"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 46139ec9-7095-481a-bf45-20200a2fdc03
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Deleting Rows by Bookmark with SQLBulkOperations
When deleting a row by bookmark, **SQLBulkOperations** makes the data source delete one or more selected rows of the table. The rows are identified by the bookmark in a bound bookmark column.  
  
 To delete rows by bookmark with **SQLBulkOperations**, the application does the following:  
  
1.  Retrieves and caches the bookmarks of all rows to be deleted. If there is more than one bookmark and column-wise binding is used, the bookmarks are stored in an array; if there is more than one bookmark and row-wise binding is used, the bookmarks are stored in an array of row structures.  
  
2.  Sets the SQL_ATTR_ROW_ARRAY_SIZE statement attribute to the number of bookmarks and binds the buffer containing the bookmark value, or the array of bookmarks, to column 0.  
  
3.  Calls **SQLBulkOperations** with *Operation* set to SQL_DELETE_BY_BOOKMARK.