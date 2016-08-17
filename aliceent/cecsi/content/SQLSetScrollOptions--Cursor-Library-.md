---
title: "SQLSetScrollOptions (Cursor Library)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c5c0ac6d-a6c1-4077-8186-1644df1944f8
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLSetScrollOptions (Cursor Library)
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work and plan to modify applications that currently use this feature. Microsoft recommends using the driver's cursor functionality.  
  
 This topic discusses the use of the **SQLSetScrollOptions** function in the cursor library. For general information about **SQLSetScrollOptions**, see [SQLSetScrollOptions Function](../content/SQLSetScrollOptions-Function.md).  
  
 The cursor library supports **SQLSetScrollOptions** only for backward compatibility; applications should use the SQL_ATTR_CONCURRENCY, SQL_ATTR_CURSOR_TYPE, and SQL_ATTR_ROW_ARRAY_SIZE statement attributes instead.