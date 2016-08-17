---
title: "SQLAllocConnect (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 70d48b12-def5-475c-b8e1-654a55fdfe0f
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLAllocConnect (Visual FoxPro ODBC Driver)
> [!NOTE]  
>  This topic contains Visual FoxPro ODBC Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Support: Full  
  
 ODBC API Conformance: Core Level  
  
 Allocates memory for a connection handle, *hdbc*, within the environment identified by *henv*. The Driver Manager processes this call and calls the driver's **SQLAllocConnect** whenever [SQLConnect](../content/SQLConnect--Visual-FoxPro-ODBC-Driver-.md), **SQLBrowseConnect**, or [SQLDriverConnect](../content/SQLDriverConnect--Visual-FoxPro-ODBC-Driver-.md) is called.  
  
 For more information, see [SQLAllocConnect](../content/SQLAllocConnect-Function.md) in the *ODBC Programmer's Reference*.