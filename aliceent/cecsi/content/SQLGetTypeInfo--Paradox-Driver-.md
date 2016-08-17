---
title: "SQLGetTypeInfo (Paradox Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e65063c7-ba9e-4cf0-ac13-4bb5bd2937db
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLGetTypeInfo (Paradox Driver)
> [!NOTE]  
>  This topic provides Paradox Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 The name of the type (TYPE_NAME) returned in the table produced by **SQLGetTypeInfo** will be the name most commonly used by the data source.  
  
 SQL_ALL_EXCEPT_LIKE will be returned in the SEARCHABLE column for the Byte, Counter, Double, Single, Long, and Short data types. (The LIKE capability can be achieved by converting the value to a character using the ODBC canonical conversion functions, and then performing the comparison.)