---
title: "SQLGetStmtOption (Cursor Library)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 986170b3-fba8-4323-9224-60b381c7effb
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLGetStmtOption (Cursor Library)
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work and plan to modify applications that currently use this feature. Microsoft recommends using the driver's cursor functionality.  
  
 This topic discusses the use of the **SQLGetStmtOption** function in the cursor library. For general information about **SQLGetStmtOption**, see [SQLGetStmtOption Function](../content/SQLGetStmtOption-Function.md).  
  
 The cursor library supports the following statement options with **SQLGetStmtOption**:  
  
|||  
|-|-|  
|SQL_BIND_TYPE|SQL_ROW_NUMBER|  
|SQL_CONCURRENCY|SQL_ROWSET_SIZE|  
|SQL_CURSOR_TYPE|SQL_SIMULATE_CURSOR|  
|SQL_GET_BOOKMARK||