---
title: "SQLGetStmtOption (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 984a8b1d-f12c-420c-8be4-f555114c764b
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLGetStmtOption (Visual FoxPro ODBC Driver)
> [!NOTE]  
>  This topic contains Visual FoxPro ODBC Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Support: Full  
  
 ODBC API Conformance: Level One  
  
 Returns the current setting of a statement option.  
  
|*FOption*|Returns|  
|---------------|-------------|  
|SQL_GET_BOOKMARK|32-bit integer value that is the bookmark for the current record number|  
|SQL_ROW_NUMBER|32-bit integer specifying the position of the current row within the result set|  
|SQL_TRANSLATE_DLL|Error: "Driver not capable"|  
  
 The Visual FoxPro ODBC Driver has no translation DLLs.  
  
 For more information, see [SQLGetStmtOption](../content/SQLGetStmtOption-Function.md) in the *ODBC Programmer's Reference*.