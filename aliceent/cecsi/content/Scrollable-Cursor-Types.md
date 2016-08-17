---
title: "Scrollable Cursor Types"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dbd32576-0453-4e90-ae45-1a81cee8259d
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Scrollable Cursor Types
The four types of scrollable cursors are static, dynamic, keyset-driven, and mixed. Static cursors detect few or no changes but are relatively cheap to implement. Dynamic cursors detect all changes but are expensive to implement. Keyset-driven and mixed cursors lie in between, detecting most changes but at less expense than dynamic cursors.  
  
 The following terms are used to define the characteristics of each type of scrollable cursor:  
  
-   **Own updates, deletes, and inserts.** Updates, deletes, and inserts made through the cursor, either with a call to **SQLBulkOperations** or **SQLSetPos** or with a positioned update or delete statement.  
  
-   **Other updates, deletes, and inserts.** Updates, deletes, and inserts not made by the cursor, including those made by other operations in the same transaction, those made through other transactions, and those made by other applications.  
  
-   **Membership.** The set of rows in the result set.  
  
-   **Order.** The order in which rows are returned by the cursor.  
  
-   **Values.** The values in each row in the result set.  
  
 For information about how to update, delete, and insert data, see [Updating Data Overview](../content/Updating-Data-Overview.md).  
  
 This section contains the following topics.  
  
-   [ODBC Static Cursors](../content/ODBC-Static-Cursors.md)  
  
-   [ODBC Dynamic Cursors](../content/ODBC-Dynamic-Cursors.md)  
  
-   [Keyset-Driven Cursors](../content/Keyset-Driven-Cursors.md)  
  
-   [Mixed Cursors](../content/Mixed-Cursors.md)