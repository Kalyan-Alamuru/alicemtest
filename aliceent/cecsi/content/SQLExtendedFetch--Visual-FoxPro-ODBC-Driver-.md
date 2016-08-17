---
title: "SQLExtendedFetch (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b28af112-fb47-4143-b11e-3b743b2ae1b8
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLExtendedFetch (Visual FoxPro ODBC Driver)
> [!NOTE]  
>  This topic contains Visual FoxPro ODBC Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Support: Full  
  
 ODBC API Conformance: Level 2  
  
 Similar to [SQLFetch](../content/SQLFetch--Visual-FoxPro-ODBC-Driver-.md) but returns multiple rows using an array for each column. The result set is forward-scrollable and can be made backward-scrollable if the cursor is defined to be static, not forward-only.  
  
 By default, the Visual FoxPro ODBC Driver does not return rows marked as deleted in a FoxPro table. Rows marked for deletion but not yet removed from a table are not included in the result set cursor. You can change this behavior by using the [SET DELETED](../content/SET-DELETED-Command.md) command.  
  
 For more information, see [SQLExtendedFetch](../content/SQLExtendedFetch-Function.md) in the *ODBC Programmer's Reference*.