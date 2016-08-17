---
title: "SQL to C: GUID"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cf56c684-c261-4b89-994a-db14ab2241d6
caps.latest.revision: 7
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQL to C: GUID
The identifier for the GUID ODBC SQL data type is:  
  
 SQL_GUID  
  
 The following table shows the ODBC C data types to which GUID SQL data may be converted. For an explanation of the columns and terms in the table, see [Converting Data from SQL to C Data Types](../content/Converting-Data-from-SQL-to-C-Data-Types.md).  
  
|C type identifier|Test|**TargetValuePtr*|**StrLen_or_IndPtr*|SQLSTATE|  
|-----------------------|----------|------------------------|----------------------------|--------------|  
|SQL_C_CHAR|*BufferLength* > Character byte length|Data|36|n/a|  
||*BufferLength* < 37|Undefined|Undefined|22003|  
|SQL_C_WCHAR|*BufferLength* > Character length|Data|36|n/a|  
||*BufferLength* < 37|Undefined|Undefined|22003|  
|SQL_C_BINARY|Byte length of data <= *BufferLength*|Data|Length of data in bytes|n/a|  
||Byte length of data > *BufferLength*|Undefined|Undefined|22003|  
|SQL_C_GUID|None[a]|Data|16[b]|n/a|  
  
 [a]   The value of *BufferLength* is ignored for this conversion. The driver assumes that the size of **TargetValuePtr* is the size of the C data type.  
  
 [b]   This is the size of the corresponding C data type.