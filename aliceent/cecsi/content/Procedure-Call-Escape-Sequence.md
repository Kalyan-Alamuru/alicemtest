---
title: "Procedure Call Escape Sequence"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 269fbab0-e5f2-4a98-86c0-2d7b647acaae
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Procedure Call Escape Sequence
ODBC uses escape sequences for procedure calls. The syntax of this escape sequence is as follows:  
  
 **{**[?=]**call** *procedure-name*[**(**[*parameter*][,[*parameter*]]...**)**]**}**  
  
 In BNF notation, the syntax is as follows:  
  
 *ODBC-procedure-escape* ::=  
  
 &#124; *ODBC-esc-initiator* [?=] call *procedure ODBC-esc-terminator*  
  
 *procedure* ::= *procedure-name* &#124; *procedure-name* (*procedure-parameter-list*)  
  
 *procedure-identifier* ::= *user-defined-name*  
  
 *procedure-name* ::= *procedure-identifier*  
  
 &#124; *owner-name*.*procedure-identifier*  
  
 &#124; *catalog-name catalog-separator* *procedure-identifier*  
  
 &#124; *catalog-name catalog-separator* [*owner-name*].*procedure-identifier*  
  
 (The third syntax is valid only if the data source does not support owners.)  
  
 *owner-name* ::= *user-defined-name*  
  
 *catalog-name* ::= *user-defined-name*  
  
 *catalog-separator* ::= {*implementation-defined*}  
  
 (The catalog separator is returned through **SQLGetInfo** with the SQL_CATALOG_NAME_SEPARATOR information option.)  
  
 *procedure-parameter-list* ::= *procedure-parameter*  
  
 &#124; *procedure-parameter*, *procedure-parameter-list*  
  
 *procedure-parameter* ::= *dynamic-parameter* &#124; *literal* &#124; *empty-string*  
  
 *empty-string* ::=  
  
 *ODBC-esc-initiator* ::= {  
  
 *ODBC-esc-terminator* ::= }  
  
 (If a procedure parameter is an empty string, the procedure uses the default value for that parameter.)  
  
 To determine whether the data source supports procedures and the driver supports the ODBC procedure invocation syntax, an application can call **SQLGetInfo** with the SQL_PROCEDURES information type.