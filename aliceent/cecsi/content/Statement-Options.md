---
title: "Statement Options"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cd73b769-c8b5-43e0-9f80-b3011b7a6162
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Statement Options
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work, and plan to modify applications that currently use this feature. Instead, use the ODBC driver provided by Oracle.  
  
 These options allow customization of a specific execution statement within an application.  
  
|Statement option|Notes|  
|----------------------|-----------|  
|SQL_BIND_TYPE|Cannot exceed 2,147,483,647 bytes or available memory.|  
|SQL_CONCURRENCY|For allowed values, see the [Cursor Type and Concurrency Combinations](../content/Cursor-Type-and-Concurrency-Combinations.md).|  
|SQL_CURSOR_TYPE|The driver does not allow SQL_CURSOR_DYNAMIC. See [SQLSetScrollOptions](../content/Level-2-API-Functions--ODBC-Driver-for-Oracle-.md) for more information. For allowed values, see the [Cursor Type and Concurrency Combinations](../content/Cursor-Type-and-Concurrency-Combinations.md).|  
|SQL_GET_BOOKMARK|Returns a 32-bit integer value that is the bookmark for the current record number. Get only; cannot Set.|  
|SQL_KEYSET_SIZE|Can be set only to 0.|  
|SQL_MAX_ROWS|The maximum number of rows to return from a result set.|  
|SQL_ROW_NUMBER|Returns a 32-bit integer specifying the position of the current row within the result set. Get only; cannot Set.|  
|SQL_ROWSET_SIZE|Cannot exceed 4,294,967,296 rows; however, you must have enough virtual memory in your computer to handle your request.|  
|SQL_USE_BOOKMARKS|Supports setting SQL_USE_BOOKMARKS to SQL_UB_ON and exposes fixed-length bookmarks.|