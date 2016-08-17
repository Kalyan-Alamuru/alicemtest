---
title: "SQL Conformance Levels (ODBC Driver for Oracle)"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 077a6c6a-2c57-42c9-a4fd-4cf0e65cf7e2
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQL Conformance Levels (ODBC Driver for Oracle)
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work, and plan to modify applications that currently use this feature. Instead, use the ODBC driver provided by Oracle.  
  
 The ODBC Driver for Oracle supports the Minimum SQL grammar and Core SQL grammar and also supports the following ODBC extensions to SQL:  
  
-   Date, time, and timestamp data  
  
-   Left and right outer joins  
  
-   Numeric functions:  
  
    |||||  
    |-|-|-|-|  
    |Abs|Log|round|tan|  
    |Ceiling|Log10|second|truncate|  
    |Cos|Mod|sign||  
    |Exp|Pi|sin||  
    |Floor|Power|sqrt||  
  
-   Date functions:  
  
    |||||  
    |-|-|-|-|  
    |Curdate|Dayofweek|monthname|second|  
    |Curtime|Dayofyear|minute|week|  
    |Dayname|Hour|now|year|  
    |Dayofmonth|Month|quarter||  
  
-   String functions:  
  
    |||||  
    |-|-|-|-|  
    |Ascii|Left|right|ucase|  
    |Char|Length|rtrim||  
    |Concat|Ltrim|soundex||  
    |Lcase|Replace|substring||  
  
-   Type-conversion function:  
  
    ||  
    |-|  
    |Convert|  
  
-   System functions:  
  
    ||  
    |-|  
    |Ifnull|  
    |User|