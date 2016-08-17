---
title: "Scalar Function Escape Sequence"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: aaf5d516-e090-445f-8839-9e39581c69c7
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Scalar Function Escape Sequence
ODBC uses escape sequences for scalar functions. The syntax of this escape sequence is as follows:  
  
```  
{fn scalar-function}  
```  
  
## Remarks  
 In BNF notation, the syntax is as follows:  
  
 *ODBC-scalar-function-escape* ::=  
  
 *ODBC-esc-initiator* fn *scalar-function ODBC-esc-terminator*  
  
 *scalar-function* ::= *function-name* (*argument-list*)  
  
 (The definitions for the nonterminals *function-name* and *function-name* (*argument-list*) are derived from the list of scalar functions in [Appendix E: Scalar Functions](../Topic/Appendix%20E:%20Scalar%20Functions.md).)  
  
 *ODBC-esc-initiator* ::= {  
  
 *ODBC-esc-terminator* ::= }  
  
 To determine whether the data source supports procedures and the driver supports the ODBC procedure invocation syntax, an application can call **SQLGetInfo**. For more information, see [Appendix E: Scalar Functions](../Topic/Appendix%20E:%20Scalar%20Functions.md).