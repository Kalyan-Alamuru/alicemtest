---
title: "DDL Statements"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 96ac9859-5976-4b06-ae1f-2fec3231e266
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# DDL Statements
Data Definition Language (DDL) statements vary tremendously among DBMSs. ODBC SQL defines statements for the most common data definition operations: creating and dropping tables, indexes, and views; altering tables; and granting and revoking privileges. All other DDL statements are data source–specific. Therefore, interoperable applications cannot perform some data definition operations. In general, this is not a problem, because such operations tend to be highly DBMS-specific and are best left to the proprietary database administration software shipped with most DBMSs or the setup program shipped with the driver.  
  
 Another problem in data definition is that data type names vary tremendously among DBMSs. Rather than defining standard data type names and forcing drivers to convert them to DBMS-specific names, **SQLGetTypeInfo** provides a way for applications to discover DBMS-specific data type names. Interoperable applications should use these names in SQL statements to create and alter tables; the names listed in [Appendix C: SQL Grammar](../Topic/Appendix%20C:%20SQL%20Grammar.md), and [Appendix D: Data Types](../Topic/Appendix%20D:%20Data%20Types.md), are examples only.