---
title: "Cursor Type and Concurrency Combinations"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: db63d610-f86f-4029-9d66-fed616c8a818
caps.latest.revision: 9
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Cursor Type and Concurrency Combinations
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work, and plan to modify applications that currently use this feature. Instead, use the ODBC driver provided by Oracle.  
  
 Cursor types control the functionality of the cursor provided to the user. Concurrency options control the updatability and locking behavior of a result set.  
  
|Cursor type|Concurrency (allowed values)|  
|-----------------|------------------------------------|  
|SQL_CURSOR_FORWARD_ONLY|SQL_CONCUR_READ_ONLY|  
|SQL_CURSOR_STATIC|SQL_CONCUR_READ_ONLY|  
|SQL_CURSOR_KEYSET_DRIVEN<sup>[1]</sup>|SQL_CONCUR_READ_ONLY SQL_CONCUR_LOCK<sup>[2]</sup> SQL_CONCUR_VALUES|  
  
 <sup>[1]</sup> See [Limitations of Using Keyset-Driven Cursors](../content/Limitations-of-Using-Keyset-Driven-Cursors.md).  
  
 <sup>[2]</sup> SQL_CONCUR_LOCK is supported only when the SQL_AUTOCOMMIT connection option is set to SQL_AUTOCOMMIT_OFF.  
  
## See Also  
 [Connect Options](../content/Connect-Options.md)