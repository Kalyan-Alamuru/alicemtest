---
title: "Inserting Rows with SQLBulkOperations"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ed585ea7-4d56-4df9-8dc3-53ca82382450
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Inserting Rows with SQLBulkOperations
Inserting data with **SQLBulkOperations** is similar to updating data with **SQLBulkOperations** because it uses data from the bound application buffers.  
  
 So that each column in the new row has a value, all bound columns with a length/indicator value of SQL_COLUMN_IGNORE and all unbound columns must either accept NULL values or have a default.  
  
 To insert rows with **SQLBulkOperations**, the application does the following:  
  
1.  Sets the SQL_ATTR_ROW_ARRAY_SIZE statement attribute to the number of rows to insert and places the new data values in the bound application buffers. For information on how to send long data with **SQLBulkOperations**, see [Long Data and SQLSetPos and SQLBulkOperations](../content/Long-Data-and-SQLSetPos-and-SQLBulkOperations.md).  
  
2.  Sets the value in the length/indicator buffer of each column as necessary. This is the byte length of the data or SQL_NTS for columns bound to string buffers, the byte length of the data for columns bound to binary buffers, and SQL_NULL_DATA for any columns to be set to NULL. The application sets the value in the length/indicator buffer of those columns that are to be set to their default (if one exists) or NULL (if one does not) to SQL_COLUMN_IGNORE.  
  
3.  Calls **SQLBulkOperations** with the *Operation* argument set to SQL_ADD.  
  
 After **SQLBulkOperations** returns, the current row is unchanged. If the bookmark column (column 0) is bound, **SQLBulkOperations** returns the bookmarks of the inserted rows in the rowset buffer bound to that column.