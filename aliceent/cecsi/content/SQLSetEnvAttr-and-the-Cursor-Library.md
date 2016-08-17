---
title: "SQLSetEnvAttr and the Cursor Library"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 59cc8eae-09ae-4796-869a-c5806488ae83
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLSetEnvAttr and the Cursor Library
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work and plan to modify applications that currently use this feature. Microsoft recommends using the driver's cursor functionality.  
  
 This topic discusses the use of the **SQLSetEnvAttr** function with the cursor library. For general information about **SQLSetEnvAttr**, see [SQLSetEnvAttr Function](../content/SQLSetEnvAttr-Function.md).  
  
 The cursor library is unaffected by the setting of the SQL_ATTR_ODBC_VERSION environment attribute, regardless of the application version or driver version.