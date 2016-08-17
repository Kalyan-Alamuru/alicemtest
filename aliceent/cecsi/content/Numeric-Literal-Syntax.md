---
title: "Numeric Literal Syntax"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fb17498d-4f1d-4b3d-b33d-1e62c7d3c32d
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Numeric Literal Syntax
The following syntax is used for numeric literals in ODBC:  
  
 *numeric-literal* ::= *signed-numeric-literal &#124; unsigned-numeric-literal*  
  
 *signed-numeric-literal* ::= [*sign*] *unsigned-numeric-literal*  
  
 *unsigned-numeric-literal* ::= *exact-numeric-literal &#124; approximate-numeric-literal*  
  
 *exact-numeric-literal* ::= *unsigned-integer* [*period*[*unsigned-integer*]] *&#124;period unsigned-integer*  
  
 *sign* ::= *plus-sign &#124; minus-sign*  
  
 *approximate-numeric-literal* ::= *mantissa E exponent*  
  
 *mantissa* ::= *exact-numeric-literal*  
  
 *exponent* ::= *signed-integer*  
  
 *signed-integer* ::= [*sign*] *unsigned-integer*  
  
 *unsigned-integer* ::= *digit...*  
  
 *plus-sign* ::= *+*  
  
 *minus-sign* ::= -  
  
 *digit* ::= 1 &#124; 2 &#124; 3 &#124; 4 &#124; 5 &#124; 6 &#124; 7 &#124; 8 &#124; 9 &#124; 0  
  
 *period* ::= .