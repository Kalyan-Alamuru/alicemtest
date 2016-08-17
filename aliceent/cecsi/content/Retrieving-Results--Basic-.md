---
title: "Retrieving Results (Basic)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 052870e3-3f3f-4f07-91da-b649348225f4
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Retrieving Results (Basic)
A *result set* is a set of rows on the data source that matches certain criteria. It is a conceptual table that results from a query and that is available to an application in tabular form. **SELECT** statements, catalog functions, and some procedures create result sets. In the following example, the first SQL statement creates a result set containing all the rows and all the columns in the Orders table, and the second SQL statement creates a result set containing OrderID, SalesPerson, and Status columns for the rows in the Orders table in which the Status is OPEN:  
  
```  
SELECT * FROM Orders  
SELECT OrderID, SalesPerson, Status FROM Orders WHERE Status = 'OPEN'  
```  
  
 A result set can be empty, which is different from no result set at all. For example, the following SQL statement creates an empty result set:  
  
```  
SELECT * FROM Orders WHERE 1 = 2  
```  
  
 An empty result set is no different from any other result set except that it has no rows. For example, the application can retrieve metadata for the result set, can attempt to fetch rows, and must close the cursor over the result set.  
  
 The process of retrieving rows from the data source and returning them to the application is called *fetching*. This section explains the basic parts of that process. For information about more advanced topics, such as block and scrollable cursors, see [Block Cursors](../content/Block-Cursors.md) and [Scrollable Cursors](../content/Scrollable-Cursors.md). For information about updating, deleting, and inserting rows, see [Updating Data Overview](../content/Updating-Data-Overview.md).  
  
 This section contains the following topics.  
  
-   [Was a Result Set Created?](../content/Was-a-Result-Set-Created-.md)  
  
-   [Result Set Metadata](../content/Result-Set-Metadata.md)  
  
-   [Binding Columns](../content/Binding-Columns.md)  
  
-   [Fetching Data](../content/Fetching-Data.md)  
  
-   [Closing the Cursor](../content/Closing-the-Cursor.md)