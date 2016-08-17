---
title: "SQLRowCount (Cursor Library)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 781cf5a5-325e-4523-8633-d96d9e98277c
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLRowCount (Cursor Library)
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work and plan to modify applications that currently use this feature. Microsoft recommends using the driver's cursor functionality.  
  
 This topic discusses the use of the **SQLRowCount** function in the cursor library. For general information about **SQLRowCount**, see [SQLRowCount Function](../content/SQLRowCount-Function.md).  
  
 When an application calls **SQLRowCount** with the statement associated with the cursor, the cursor library returns the number of rows of data it has retrieved from the driver.  
  
 When an application calls **SQLRowCount** with the statement associated with a positioned update or delete statement, the cursor library returns the number of rows affected by the statement.  
  
 When an application calls **SQLRowCount** after a **SELECT** statement, the cursor library returns –1.