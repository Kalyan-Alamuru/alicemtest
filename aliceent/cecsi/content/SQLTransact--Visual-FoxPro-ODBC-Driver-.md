---
title: "SQLTransact (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 92cf86c0-f7a8-44d7-b59f-a1342677440b
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLTransact (Visual FoxPro ODBC Driver)
> [!NOTE]  
>  This topic contains Visual FoxPro ODBC Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Support: Full  
  
 ODBC API Conformance: Core Level  
  
 Requests a commit or rollback operation for all active operations on all statement handles (*hstmt*s) associated with a connection or for all connections associated with the environment handle, *henv*. **SQLTransact** works only for data sources that are [databases](../content/Visual-FoxPro-Terminology.md).  
  
 If a commit fails when in manual mode, the transaction remains active; you can choose to roll back the transaction or retry the commit operation. If a commit operation fails when in automatic transaction mode, the transaction is rolled back automatically; the transaction cannot be inactive.  
  
 For more information, see [SQLTransact](../content/SQLTransact-Function.md) in the *ODBC Programmer's Reference*.