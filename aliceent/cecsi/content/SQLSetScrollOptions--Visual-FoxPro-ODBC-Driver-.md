---
title: "SQLSetScrollOptions (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 693e6e28-a845-41b1-9622-5058b0d87229
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLSetScrollOptions (Visual FoxPro ODBC Driver)
> [!NOTE]  
>  This topic contains Visual FoxPro ODBC Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Support: Partial  
  
 ODBC API Conformance: Level 2  
  
 Sets options that control the behavior of cursors associated with a statement handle, *hstmt*.  
  
 The Visual FoxPro ODBC Driver supports only SQL_CONCUR_READ_ONLY; it does not support the *fConcurrency* value SQL_CONCUR_ROWVER. The driver converts SQL_KEYSET_SIZE, SQL_CURSOR_DYNAMIC, and SQL_CURSOR_KEYSET_DRIVEN to SQL_SCROLL_STATIC with warning ODBC_01S02.  
  
 For more information, see [SQLSetScrollOptions](../content/SQLSetScrollOptions-Function.md) in the *ODBC Programmer's Reference*.