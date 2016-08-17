---
title: "Data Type Limitations"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 81c4eab7-1f6b-47a0-b940-89d6c6a14dae
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Data Type Limitations
The Microsoft ODBC Desktop Database Drivers impose the following limitations on data types:  
  
|Data type|Description|  
|---------------|-----------------|  
|All data types|Type conversion failures might result in the affected column being set to NULL.|  
|BINARY|Creating a zero-length BINARY column actually returns a 255-byte BINARY column.|  
|DATE|The DATE data type cannot be converted to another data type (or itself) by the CONVERT function.|  
|DECIMAL (Exact Numeric)|Not supported.|  
|Floating-Point Data Types|The number of decimal places in a floating-point number may be limited by the number format set in the International section of the Windows Control Panel.|  
|NUMERIC|Supports maximum precision and a scale of 28.|  
|TIMESTAMP|The TIMESTAMP data type cannot be converted to itself by the CONVERT function.|  
|TINYINT|TINYINT values are always unsigned.|  
|Zero-Length Strings|When a dBASE, Microsoft Excel, Paradox, or Textdriver is used, inserting a zero-length string into a column actually inserts a NULL instead.|