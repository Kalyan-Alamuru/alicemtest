---
title: "SQLSetParam Mapping"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 022dfbc0-8d18-4c35-8a28-d9eb16063188
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLSetParam Mapping
**SQLSetParam** continues to be mapped on top of **SQLBindParameter** as in ODBC 2.*x*. Even though it is conceptually similar to **SQLBindParam**, the Driver Manager does not map **SQLSetParam** to **SQLBindParam**. This is because certain existing ODBC 2.*x* drivers use the special value of *BufferLength* (SQL_SETPARAM_VALUE_MAX) that the Driver Manager generates when it maps **SQLSetParam** on top of **SQLBindParameter** to determine when it is called by a 1.*x* ODBC application.  
  
 A call to  
  
```  
SQLSetParam(hstmt, ipar, fCType, fSqlType, cbColDef, ibScale, rgbValue, pcbValue)  
```  
  
 will result in the following:  
  
```  
SQLBindParameter(StatementHandle, ParameterNumber, SQL_PARAM_INPUT_OUTPUT, ValueType, ParameterType, ColumnSize, DecimalDigits, ParameterValuePtr, SQL_SETPARAM_VALUE_MAX, StrLen_or_IndPtr)  
```