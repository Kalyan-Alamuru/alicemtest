---
title: "SQL Conformance Levels"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3529df2c-a09b-4c16-9c60-eae7a06d903a
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQL Conformance Levels
The level of SQL-92 grammar supported by a driver is indicated by the value returned by a call to **SQLGetInfo** with the SQL_SQL_CONFORMANCE information type. This indicates whether the driver conforms to the Entry, FIPS Transitional, Intermediate, or Full levels defined in SQL-92.  
  
 All ODBC drivers must support the minimum SQL grammar described in [SQL Minimum Grammar](../content/SQL-Minimum-Grammar.md) in Appendix C: SQL Grammar. This grammar is a subset of the Entry level of SQL-92. Drivers may support additional SQL and be conformant to the SQL-92 Entry, Intermediate, or Full level, or to the FIPS 127-2 Transitional level. Drivers that comply to a given level of SQL-92 or FIPS 127-2 can support additional features in any of the higher levels yet not be fully conformant to that level. To determine whether a feature is supported, an application should call **SQLGetInfo** with the appropriate information type. The conformance level of an SQL feature is described in the corresponding information type. (See the [SQLGetInfo](../content/SQLGetInfo-Function.md) function description.)