---
title: "SQLParamOptions (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7f94a6e2-9c34-405c-b2b0-304d94269715
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLParamOptions (Visual FoxPro ODBC Driver)
> [!NOTE]  
>  This topic contains Visual FoxPro ODBC Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Support: Full  
  
 ODBC API Conformance: Level 1  
  
 Allows an application to specify multiple values for the set of parameters assigned by [SQLBindParameter](../content/SQLBindParameter--Visual-FoxPro-ODBC-Driver-.md). The ability to specify multiple values for a set of parameters is useful for bulk inserts and other work that requires the data source to process the same SQL statement multiple times with various parameter values. For example, an application can specify three sets of values for the set of parameters associated with an **INSERT** statement and then execute the **INSERT** statement once to perform the three insert operations.  
  
 For more information, see [SQLParamOptions](../content/SQLParamOptions-Function.md) in the *ODBC Programmer's Reference*.