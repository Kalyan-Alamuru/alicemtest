---
title: "Type Identifiers"
ms.custom: na
ms.date: 08/05/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1d9fdfa2-e378-44fe-ac66-9743d9bbdd5a
caps.latest.revision: 9
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Type Identifiers
To describe SQL and C data types, ODBC defines two sets of *type identifiers*. A type identifier describes the type of an SQL column or a C buffer. It is a **#define** value and is generally passed as a function argument or returned in metadata.  
  
 For example, the following call to **SQLBindParameter** binds a variable of type SQL_DATE_STRUCT to a date parameter in an SQL statement. The C type identifier SQL_C_TYPE_DATE specifies the type of the *Date* variable, and the SQL type identifier SQL_TYPE_DATE specifies the type of the dynamic parameter.  
  
```  
SQL_DATE_STRUCT Date;  
SQLINTEGER  DateInd = 0;  
SQLBindParameter(hstmt, 1, SQL_PARAM_INPUT, SQL_C_TYPE_DATE, SQL_TYPE_DATE, 0, 0,  
                  &Date, 0, &DateInd);  
```