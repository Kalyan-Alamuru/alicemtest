---
title: "SQLExecDirect (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5004060f-8510-4018-87a4-d41789e69d3e
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLExecDirect (Visual FoxPro ODBC Driver)
> [!NOTE]  
>  This topic contains Visual FoxPro ODBC Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Support: Full  
  
 ODBC API Conformance: Core Level  
  
 Executes a new, [preparable SQL statement](../content/Visual-FoxPro-Terminology.md). The Visual FoxPro ODBC Driver uses the current values of the parameter marker variables if any parameters exist in the statement.  
  
 To create a batch command to submit more than one SQL statement at a time, use a semicolon (;) to separate each SQL statement in the batch.  
  
 If your table, view, or field names contain spaces, enclose the names in back quote marks. For example, if your database contains a table named My Table and the field My Field, enclose each element of the identifier as follows:  
  
```  
SELECT `My Table`.`Field1`, `My Table`.`Field2` FROM `My Table`  
```  
  
 For more information, see [SQLExecDirect](../content/SQLExecDirect-Function.md) in the *ODBC Programmer's Reference*.