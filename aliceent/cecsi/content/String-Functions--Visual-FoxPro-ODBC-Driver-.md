---
title: "String Functions (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1974fd26-ef0d-45d5-860b-298917c8e9c3
caps.latest.revision: 8
manager: jhubbard
---
# String Functions (Visual FoxPro ODBC Driver)
The following table lists ODBC string manipulation functions supported by the Visual FoxPro ODBC Driver; when the Visual FoxPro grammar for the same function differs from the ODBC syntax, the Visual FoxPro equivalent is listed.  
  
|ODBC grammar|Visual FoxPro grammar|  
|------------------|---------------------------|  
|ASCII *(string_exp)*|ASC *(string_exp)*|  
|CHAR *(code)*|CHR *(string_exp)*|  
|CONCAT *(string_exp1, string_exp2)*|*string_exp1 + string_exp2*|  
|DIFFERENCE *(string_exp1, string_exp2)*||  
|INSERT *(string_exp1, start, length, string_exp2)*|STUFF *(string_exp1, start, length, string_exp2)*|  
|LCASE *(string_exp)*|LOWER *(string_exp)*|  
|LEFT *(string_exp, count)*||  
|LENGTH *(string_exp)*|LEN *(string_exp)*|  
|LTRIM *(string_exp)*||  
|REPEAT *(string_exp, count)*|REPLICATE *(string_exp, count)*|  
|REPLACE *(string_exp1, string_exp2, string_exp3)*|STRTRAN *(string_exp1, string_exp2, string_exp3)*|  
|RIGHT *(string_exp, count)*||  
|RTRIM *(string_exp)*||  
|SOUNDEX *(string_exp)*||  
|SPACE *(count)*||  
|SUBSTRING *(string_exp, start, length)*|SUBSTR *(string_exp, start, length)*|  
|UCASE *(string_exp)*|UPPER *(string_exp)*|