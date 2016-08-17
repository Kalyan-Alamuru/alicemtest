---
title: "SQLGetData and Block Cursors"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 12599cdc-7725-4faf-bcae-e163ea0f5851
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLGetData and Block Cursors
**SQLGetData** operates on a single column of a single row and cannot fetch an array containing data from multiple rows. This is because the primary use of **SQLGetData** is to fetch long data in parts, and there is little or no reason to do this for more than one row at a time.  
  
 To use **SQLGetData** with a block cursor, an application first calls **SQLSetPos** to position the cursor on a single row. It then calls **SQLGetData** for a column in that row. However, this behavior is optional. To determine if a driver supports the use of **SQLGetData** with block cursors, an application calls **SQLGetInfo** with the SQL_GETDATA_EXTENSIONS option.