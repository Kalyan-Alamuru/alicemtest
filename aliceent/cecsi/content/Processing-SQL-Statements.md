---
title: "Processing SQL Statements"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 54dad6a3-e86c-477b-ba7c-4e95e0385ec1
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Processing SQL Statements
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work and plan to modify applications that currently use this feature. Microsoft recommends using the driver's cursor functionality.  
  
 The ODBC cursor library passes all SQL statements directly to the driver except the following:  
  
-   Positioned update and delete statements  
  
-   **SELECT FOR UPDATE** statements  
  
-   Batched SQL statements  
  
 To execute positioned update and delete statements and to position the cursor on a row to call **SQLGetData** for that row, the cursor library constructs a searched statement that identifies the row.  
  
 This section contains the following topics.  
  
-   [Processing Positioned Update and Delete Statements](../content/Processing-Positioned-Update-and-Delete-Statements.md)  
  
-   [Processing SELECT FOR UPDATE Statements](../content/Processing-SELECT-FOR-UPDATE-Statements.md)  
  
-   [Processing Batches of SQL Statements](../content/Processing-Batches-of-SQL-Statements.md)  
  
-   [Constructing Searched Statements](../content/Constructing-Searched-Statements.md)