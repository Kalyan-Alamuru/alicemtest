---
title: "SQLSpecialColumns (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b72a978d-6a60-475a-b7d9-c424d77bbe30
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLSpecialColumns (Visual FoxPro ODBC Driver)
> [!NOTE]  
>  This topic contains Visual FoxPro ODBC Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Support: Full  
  
 ODBC API Conformance: Level 1  
  
 Retrieves the optimal set of columns that uniquely identifies a row in the table.  
  
 The Visual FoxPro ODBC Driver returns the columns that make up the primary key on the FoxPro table. (See [SQLPrimaryKeys](../content/SQLPrimaryKeys--Visual-FoxPro-ODBC-Driver-.md).) If called with *fColType* set to SQL_ROWVER, no columns are returned. **SQLSpecialColumns** works only for data sources that are [databases](../content/Visual-FoxPro-Terminology.md).  
  
 For more information, see [SQLSpecialColumns](../content/SQLSpecialColumns-Function.md) in the *ODBC Programmer's Reference*.