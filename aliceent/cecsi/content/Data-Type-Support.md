---
title: "Data Type Support"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 782b4490-372b-4366-aad7-a486fb8a07c8
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Data Type Support
ODBC drivers must support at least one of SQL_CHAR and SQL_VARCHAR. Support for other data types is determined by the driver's or data source's SQL-92 conformance level. An application should call **SQLGetTypeInfo** to determine the data types supported by the driver.  
  
 For more information on data types, see [Appendix D: Data Types](../Topic/Appendix%20D:%20Data%20Types.md).