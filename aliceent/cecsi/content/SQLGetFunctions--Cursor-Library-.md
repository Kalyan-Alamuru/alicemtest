---
title: "SQLGetFunctions (Cursor Library)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 931acd12-4eb6-4a78-9a77-157a18a9a2d0
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLGetFunctions (Cursor Library)
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work and plan to modify applications that currently use this feature. Microsoft recommends using the driver's cursor functionality.  
  
 This topic discusses the use of the **SQLGetFunctions** function in the cursor library. For general information about **SQLGetFunctions**, see [SQLGetFunctions Function](../content/SQLGetFunctions-Function.md).  
  
 When you call **SQLGetFunctions**, the cursor library returns that it supports **SQLExtendedFetch**, **SQLFetchScroll**, **SQLSetPos**, and **SQLSetScrollOptions**, in addition to the functions supported by the driver.