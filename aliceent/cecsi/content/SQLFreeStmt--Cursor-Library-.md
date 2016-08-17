---
title: "SQLFreeStmt (Cursor Library)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 47bfbd4d-9453-4609-958d-1e05794cb223
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLFreeStmt (Cursor Library)
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work and plan to modify applications that currently use this feature. Microsoft recommends using the driver's cursor functionality.  
  
 This topic discusses the use of the **SQLFreeStmt** function in the cursor library. For general information about **SQLFreeStmt**, see [SQLFreeStmt Function](../content/SQLFreeStmt-Function.md).  
  
 If an application calls **SQLFreeStmt** with the SQL_UNBIND option after it calls **SQLExtendedFetch**, **SQLFetch**, or **SQLFetchScroll**, the cursor library returns an error. Before it can unbind result set columns, an application must call **SQLCloseCursor** or **SQLFreeStmt** with the SQL_CLOSE option.