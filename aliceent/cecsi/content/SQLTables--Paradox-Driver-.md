---
title: "SQLTables (Paradox Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d68adad6-97bd-4b47-bcf9-0102aafb00d4
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLTables (Paradox Driver)
> [!NOTE]  
>  This topic provides Paradox Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
|Argument|Comments|  
|--------------|--------------|  
|*szTableOwner*|The only valid argument for *szTableOwner* is NULL because none of the drivers support owner names. With *szTableOwner* set to NULL, all tables are returned. NULL is returned in the TABLE_OWNER column.|  
|*szTableQualifier*|In the TABLE_QUALIFIER column, **SQLTables** will return the path to a directory.|  
|*SzTableType*|For Paradox files, "TABLE" is the only table type supported.|  
  
## See Also  
 [SQLTables Function](../content/SQLTables-Function.md)