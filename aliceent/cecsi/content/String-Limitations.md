---
title: "String Limitations"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ec1da65f-c69d-415d-bf75-8fda8aa2b39f
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# String Limitations
The maximum length of an SQL statement string is 65,000 characters.  
  
 When the Microsoft Access driver is used, only SQL-92 string constants (with single quotation marks, not double quotation marks) are supported.  
  
 The pipe character (&#124;) cannot be used in a string, whether the character is enclosed in back quotes or not.  
  
 For maximum interoperability, applications should pass strings in parameters, rather than passing quoted strings.