---
title: "SQLColAttributes (Text File Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 132fd1c0-1921-4a7d-910e-aedf1bff5453
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLColAttributes (Text File Driver)
> [!NOTE]  
>  This topic provides Text File Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
|Attribute|Comments|  
|---------------|--------------|  
|SQL_COLUMN_DISPLAY_SIZE|For LONGVARBINARY data, SQL_COLUMN_DISPLAY_SIZE is the maximum length of the column, not the maximum length of the column times 2.|  
|SQL_OWNER_NAME|An empty string ("") is returned in this column because owner name is not supported.|  
|SQL_QUALIFIER_NAME|The path to a directory is returned.|  
|SQL_COLUMN_SEARCHABLE|LONGVARBINARY and LONGVARCHAR columns are reported as SQL_UNSEARCHABLE.<br /><br /> Fixed-length and variable-length binary and character data types are searchable, even though LONGVARBINARY and LONGVARCHAR are not.|