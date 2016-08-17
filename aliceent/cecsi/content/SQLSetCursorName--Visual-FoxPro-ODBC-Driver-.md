---
title: "SQLSetCursorName (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2ac5a8b5-f084-405b-b0d7-546284dfa111
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLSetCursorName (Visual FoxPro ODBC Driver)
> [!NOTE]  
>  This topic contains Visual FoxPro ODBC Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Support: Full  
  
 ODBC API Conformance: Core Level  
  
 Associates a cursor name with an active statement handle, *hstmt*. **SQLSetCursorName** is included in the Visual FoxPro ODBC Driver API because it is a part of Core Level ODBC API functionality; it cannot be used with other API functions because the driver does not support positioned updates.  
  
 For more information, see [SQLSetCursorName](../content/SQLSetCursorName-Function.md) in the *ODBC Programmer's Reference*.