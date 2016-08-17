---
title: "Processing Batches of SQL Statements"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 04b93ef9-11de-47a3-8bd8-ba963c42f182
caps.latest.revision: 9
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Processing Batches of SQL Statements
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work and plan to modify applications that currently use this feature. Microsoft recommends using the driver's cursor functionality.  
  
 The cursor library does not support batches of SQL statements, including SQL statements for which the SQL_ATTR_PARAMSET_SIZE statement attribute is greater than 1. If an application submits a batch of SQL statements to the cursor library, the results are undefined.