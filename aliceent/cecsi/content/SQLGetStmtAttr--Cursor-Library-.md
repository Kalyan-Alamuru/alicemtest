---
title: "SQLGetStmtAttr (Cursor Library)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6c34e1ef-4273-4afb-a7d3-f9017ab69c5e
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLGetStmtAttr (Cursor Library)
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work and plan to modify applications that currently use this feature. Microsoft recommends using the driver's cursor functionality.  
  
 This topic discusses the use of the **SQLGetStmtAttr** function in the cursor library. For general information about **SQLGetStmtAttr**, see [SQLGetStmtAttr Function](../content/SQLGetStmtAttr-Function.md).  
  
 The cursor library supports the following statement attributes with **SQLGetStmtAttr**:  
  
|||  
|-|-|  
|SQL_ATTR_CONCURRENCY|SQL_ATTR_ROW_BIND_OFFSET_PTR|  
|SQL_ATTR_CURSOR_TYPE|SQL_ATTR_ROW_BIND_TYPE|  
|SQL_ATTR_FETCH_BOOKMARK_PTR|SQL_ATTR_ROW_NUMBER|  
|SQL_ATTR_PARAM_BIND_OFFSET_PTR|SQL_ATTR_ROW_ARRAY_SIZE|  
|SQL_ATTR_PARAM_BIND_TYPE|SQL_ATTR_SIMULATE_CURSOR|