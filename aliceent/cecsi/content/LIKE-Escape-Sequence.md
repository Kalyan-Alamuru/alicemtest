---
title: "LIKE Escape Sequence"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 798d75ea-be9d-4bef-b297-318bc327f1ca
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# LIKE Escape Sequence
ODBC uses escape sequences for the LIKE clause. The syntax of this escape sequence is as follows:  
  
```  
{'escape-character'}  
```  
  
## Remarks  
 In BNF notation, the syntax is as follows:  
  
 *ODBC-like-escape* ::=  
  
 *ODBC-esc-initiator* escape '*escape-character*' *ODBC-esc-terminator*  
  
 *escape-character* ::= *character*  
  
 *ODBC-esc-initiator* ::= {  
  
 *ODBC-esc-terminator* ::= }  
  
 To determine if the driver supports the LIKE escape sequence, an application can call **SQLGetInfo** with the SQL_LIKE_ESCAPE_CLAUSE information type.