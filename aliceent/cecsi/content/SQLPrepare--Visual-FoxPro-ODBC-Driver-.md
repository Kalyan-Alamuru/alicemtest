---
title: "SQLPrepare (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0c4cb5a4-9729-4b2e-a0c6-52027b92e8fc
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLPrepare (Visual FoxPro ODBC Driver)
> [!NOTE]  
>  This topic contains Visual FoxPro ODBC Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Support: Full  
  
 ODBC API Conformance: Core Level  
  
 Prepares an SQL statement by planning how to optimize and execute the statement. The SQL statement is compiled for execution by [SQLExecDirect](../content/SQLExecDirect--Visual-FoxPro-ODBC-Driver-.md).  
  
 If your table, view, or field names contain spaces, enclose the names in back quote (`) marks. For example, if your database contains a table named My Table and the field My Field, enclose each element of the identifier as follows:  
  
```  
SELECT * FROM `My Table`.`My Field`  
```  
  
 For more information, see [SQLPrepare](../content/SQLPrepare-Function.md) in the *ODBC Programmer's Reference*.