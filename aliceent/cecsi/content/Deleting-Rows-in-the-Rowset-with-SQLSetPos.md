---
title: "Deleting Rows in the Rowset with SQLSetPos"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3117a47d-e179-4f76-89d0-656582f1c9bb
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Deleting Rows in the Rowset with SQLSetPos
The delete operation of **SQLSetPos** makes the data source delete one or more selected rows of a table. To delete rows with **SQLSetPos**, the application calls **SQLSetPos** with *Operation* set to SQL_DELETE and *RowNumber* set to the number of the row to delete. If *RowNumber* is 0, all rows in the rowset are deleted.  
  
 After **SQLSetPos** returns, the deleted row is the current row and its status is SQL_ROW_DELETED. The row cannot be used in any further positioned operations, such as calls to **SQLGetData** or **SQLSetPos**.  
  
 When deleting all rows of the rowset (*RowNumber* is equal to 0), the application can prevent the driver from deleting certain rows by using the row operation array, in the same way as for the update operation of **SQLSetPos**. (See [Updating Rows in the Rowset with SQLSetPos](../content/Updating-Rows-in-the-Rowset-with-SQLSetPos.md).)  
  
 Every row that is deleted should be a row that exists in the result set. If the application buffers were filled by fetching and if a row status array has been maintained, its values at each of these row positions should not be SQL_ROW_DELETED, SQL_ROW_ERROR, or SQL_ROW_NOROW.