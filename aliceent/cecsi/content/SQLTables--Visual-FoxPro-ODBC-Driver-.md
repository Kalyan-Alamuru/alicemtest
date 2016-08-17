---
title: "SQLTables (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 69e2a038-5def-423f-91aa-8756e069dd2a
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLTables (Visual FoxPro ODBC Driver)
> [!NOTE]  
>  This topic contains Visual FoxPro ODBC Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Support: Full  
  
 ODBC API Conformance: Level 1  
  
 Returns the list of table names specified by the parameter in the **SQLTables** statement. If no parameter is specified, returns the table names stored in the current data source. The driver returns the information as a result set.  
  
 Enumeration type calls will not receive a result set entry for remote views or local parameterized views. However, a call to **SQLTables** with a unique table name specifier will find a match for such a view if present with that name; this allows the API to be used to check for name conflicts prior to creation of a new table.  
  
> [!NOTE]  
>  The Visual FoxPro ODBC driver differentiates between [database tables](../content/Visual-FoxPro-Terminology.md) and [free tables](../content/Visual-FoxPro-Terminology.md), even when both types of tables are stored in the same directory on your system. If your data source is a directory of free tables, the Visual FoxPro ODBC Driver does not catalog or return the names of any tables that are associated with a database.  
  
 For more information, see [SQLTables](../content/SQLTables-Function.md) in the *ODBC Programmer's Reference*.