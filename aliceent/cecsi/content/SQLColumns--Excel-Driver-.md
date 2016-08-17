---
title: "SQLColumns (Excel Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4bae3fcd-0287-4f79-ad7c-8f7ab2f6f940
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLColumns (Excel Driver)
> [!NOTE]  
>  This topic provides Excel Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
|Column|Comments|  
|------------|--------------|  
|TABLE_QUALIFIER|The path to a directory is returned.|  
|TABLE_OWNER|NULL is returned in this column because owner name is not supported.|  
|NULLABLE|SQL_NO_NULLS is returned for columns that participate in a primary key or unique index.|