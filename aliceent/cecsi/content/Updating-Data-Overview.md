---
title: "Updating Data Overview"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 062036a4-cda6-4aaa-9765-f1ec3e0b31b1
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Updating Data Overview
Applications can update data either by executing SQL statements or by calling **SQLSetPos** or **SQLBulkOperations**. **UPDATE**, **DELETE**, and **INSERT** statements act directly on the data source and are usually supported by drivers. Searched update and delete statements contain a specification of the rows to change. Positioned update and delete statements and **SQLSetPos** act on the data source through a cursor and are less widely supported.  
  
 Whether cursors can detect changes made to the result set with the methods described in this section depends on the type of the cursor and how it is implemented. Forward-only cursors do not revisit rows and therefore will not detect any changes. For information about whether scrollable cursors can detect changes, see [Scrollable Cursors](../content/Scrollable-Cursors.md).  
  
 This section contains the following topics.  
  
-   [UPDATE, DELETE, and INSERT Statements](../content/UPDATE--DELETE--and-INSERT-Statements.md)  
  
-   [Positioned Update and Delete Statements](../content/Positioned-Update-and-Delete-Statements.md)  
  
-   [Simulating Positioned Update and Delete Statements](../content/Simulating-Positioned-Update-and-Delete-Statements.md)  
  
-   [Determining the Number of Affected Rows](../content/Determining-the-Number-of-Affected-Rows.md)  
  
-   [Updating Data with SQLSetPos](../content/Updating-Data-with-SQLSetPos.md)  
  
-   [Updating Data with SQLBulkOperations](../content/Updating-Data-with-SQLBulkOperations.md)  
  
-   [Long Data and SQLSetPos and SQLBulkOperations](../content/Long-Data-and-SQLSetPos-and-SQLBulkOperations.md)