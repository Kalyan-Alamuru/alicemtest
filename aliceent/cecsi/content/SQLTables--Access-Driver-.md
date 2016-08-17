---
title: "SQLTables (Access Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 94423cf9-341a-4db6-bb10-8f5448df7fc3
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLTables (Access Driver)
> [!NOTE]  
>  This topic provides Access Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
|Argument|Comments|  
|--------------|--------------|  
|*szTableOwner*|The only valid argument for *szTableOwner* is NULL because none of the drivers support owner names. With *szTableOwner* set to NULL, all tables are returned. NULL is returned in the TABLE_OWNER column.|  
|*szTableQualifier*|In the TABLE_QUALIFIER column, **SQLTables** will return the path to a database file.|  
|*SzTableType*|When the Microsoft Access driver is used, "SYSTEM TABLE" is supported for *szTableType* for system tables, "SYNONYM" is supported for attached tables, and "VIEW" is supported for row-returning queries.|  
  
## See Also  
 [SQLTables Function](../content/SQLTables-Function.md)