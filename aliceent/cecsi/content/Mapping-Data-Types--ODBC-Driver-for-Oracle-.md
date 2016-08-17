---
title: "Mapping Data Types (ODBC Driver for Oracle)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a5d9ce12-19da-4943-8493-e3d56fa08348
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Mapping Data Types (ODBC Driver for Oracle)
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work, and plan to modify applications that currently use this feature. Instead, use the ODBC driver provided by Oracle.  
  
 The Oracle Server supports a set of data types. The ODBC Driver for Oracle maps these data types to their appropriate ODBC SQL data types. The following table lists the Oracle 7.3 Server data types and their corresponding ODBC SQL data types.  
  
 The ODBC Driver for Oracle supports Oracle 7.3 and some Oracle8 data types. For more information about supported Oracle8 data types, see [Supported Data Types](../content/Supported-Data-Types--ODBC-Driver-for-Oracle-.md).  
  
|Oracle Server data type|ODBC SQL data type|  
|-----------------------------|------------------------|  
|CHAR|SQL_CHAR|  
|DATE|SQL_TIMESTAMP|  
|FLOAT|SQL_DOUBLE|  
|INTEGER|SQL_DECIMAL|  
|LONG|SQL_LONGVARCHAR|  
|LONG RAW|SQL_LONGVARBINARY|  
|NUMBER|SQL_DECIMAL|  
|RAW|SQL_VARBINARY|  
|VARCHAR2|SQL_VARCHAR|  
  
> [!NOTE]  
>  For more information about the allowable size of the VARCHAR column, see [VARCHAR Column Size](../content/VARCHAR-Column-Size--ODBC-Driver-for-Oracle-.md) in this guide.