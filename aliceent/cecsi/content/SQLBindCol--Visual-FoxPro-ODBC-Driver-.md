---
title: "SQLBindCol (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 984d6605-39ba-4d33-ac94-22625bfa6107
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLBindCol (Visual FoxPro ODBC Driver)
> [!NOTE]  
>  This topic contains Visual FoxPro ODBC Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Support: Full  
  
 ODBC API Conformance: Core Level  
  
 Assigns storage space for a result column and specifies the type of the result. When [SQLFetch](../content/SQLFetch--Visual-FoxPro-ODBC-Driver-.md) or [SQLExtendedFetch](../content/SQLExtendedFetch--Visual-FoxPro-ODBC-Driver-.md) is called, the driver places the data for all bound columns in the assigned locations. See [SQLGetTypeInfo](../content/SQLGetTypeInfo--Visual-FoxPro-ODBC-Driver-.md) for the mapping between ODBC and Visual FoxPro data types.  
  
 For more information, see [SQLBindCol](../content/SQLBindCol-Function.md) in the *ODBC Programmer's Reference*.