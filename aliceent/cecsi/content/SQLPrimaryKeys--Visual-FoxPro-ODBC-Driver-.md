---
title: "SQLPrimaryKeys (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8dbe2903-efdc-45e0-a079-9e357c5fd81b
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLPrimaryKeys (Visual FoxPro ODBC Driver)
> [!NOTE]  
>  This topic contains Visual FoxPro ODBC Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Support: Full  
  
 ODBC API Conformance: Level 2  
  
 Returns the column names that comprise the primary key for a table. The Visual FoxPro ODBC Driver implementation of **SQLPrimaryKeys** behaves as follows:  
  
-   Ignores the *szTableOwner* and *cbTableOwner* arguments.  
  
-   Works only for data sources that are [databases](../content/Visual-FoxPro-Terminology.md). The driver returns the error "Driver does not support this function" if the data source is a directory of [free tables](../content/Visual-FoxPro-Terminology.md).  
  
 For more information, see [SQLPrimaryKeys](../content/SQLPrimaryKeys-Function.md) in the *ODBC Programmer's Reference*.