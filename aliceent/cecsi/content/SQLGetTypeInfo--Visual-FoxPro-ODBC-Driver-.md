---
title: "SQLGetTypeInfo (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5f25e20b-a4ef-42da-aeb6-00e0510fb1cc
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLGetTypeInfo (Visual FoxPro ODBC Driver)
> [!NOTE]  
>  This topic contains Visual FoxPro ODBC Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Support: Full  
  
 ODBC API Conformance: Level 1  
  
 Returns information about the data types supported by a data source. The driver returns the information in an SQL result set. The following table lists ODBC data types and the corresponding Visual FoxPro data type.  
  
|ODBC type|Visual FoxPro type|  
|---------------|------------------------|  
|SQL_BIGINT|Not supported. There is no 64-bit Visual FoxPro type.|  
|SQL_BIT|Logical|  
|SQL_CHAR|Character|  
|SQL_DATE|Date|  
|SQL_DECIMAL|Numeric|  
|SQL_DOUBLE|Double|  
|SQL_FLOAT|Double|  
|SQL_INTEGER|Integer|  
|SQL_LONGVARBINARY|Memo (Binary)|  
|SQL_LONGVARCHAR|Memo|  
|SQL_NUMERIC|Numeric*, Currency, Float|  
|SQL_REAL|Double|  
|SQL_SMALLINT|Integer|  
|SQL_TIME|Not supported. There is no Visual FoxPro *time* type.|  
|SQL_TIMESTAMP|DateTime|  
|SQL_TINYINT|Integer|  
|SQL_VARBINARY|Memo (Binary)*, General|  
|SQL_VARCHAR|Character|  
  
 *Default type  
  
 For more information about Visual FoxPro data types, see [CREATE TABLE](../content/CREATE-TABLE---SQL-Command.md). For more information about this function, see [SQLGetTypeInfo](../content/SQLGetTypeInfo-Function.md) in the *ODBC Programmer's Reference*.