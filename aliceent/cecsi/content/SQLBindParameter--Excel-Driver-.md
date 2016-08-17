---
title: "SQLBindParameter (Excel Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 40489bc5-3e2a-425e-892d-e0dc037f4d7a
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLBindParameter (Excel Driver)
> [!NOTE]  
>  This topic provides Excel Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 When the Microsoft Excel driver is used, executing an INSERT statement that uses a parameter to insert a NULL into a SQL_CHAR column will return SQL_SUCCESS_WITH_INFO with SQLSTATE 01004, "Data Truncated."