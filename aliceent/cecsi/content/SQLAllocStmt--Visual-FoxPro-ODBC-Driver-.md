---
title: "SQLAllocStmt (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ba973025-18c8-481b-a383-6ed935237894
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLAllocStmt (Visual FoxPro ODBC Driver)
> [!NOTE]  
>  This topic contains Visual FoxPro ODBC Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Support: Full  
  
 ODBC API Conformance: Core Level  
  
 Allocates memory for a statement handle and associates the statement handle with the connection specified by *hdbc*. The Driver Manager passes this call to the driver, which allocates the memory for the *hstmt* structure.  
  
 For more information, see [SQLAllocStmt](../content/SQLAllocStmt-Function.md) in the *ODBC Programmer's Reference*.