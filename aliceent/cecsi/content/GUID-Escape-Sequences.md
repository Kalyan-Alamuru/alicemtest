---
title: "GUID Escape Sequences"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 71d43ef9-4a31-493e-b9e0-f864e9ef3ce6
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# GUID Escape Sequences
ODBC uses escape sequences for GUID literals. The syntax of this escape sequence is as follows:  
  
```  
{guid 'nnnnnnnn-nnnn-nnnn-nnnn-nnnnnnnnnnnn'}  
```  
  
## Remarks  
 In BNF notation, the syntax is as follows:  
  
 *ODBC-guid-escape* ::=  
     *ODBC-esc-initiator guid* '*guid-value*' *ODBC-esc-terminator*  
  
 *ODBC-esc-initiator* ::= {  
  
 *ODBC-esc-terminator* ::= }  
  
 *guid-value* ::= *clock-low-value guid-separator clock-middle-value guid-separator clock-high-value guid-separator clock-seq-value guid-separator node-value*  
  
 *guid-separator* ::= -  
  
 *clock-low-value* ::= *hex_digit hex_digit hex_digit hex_digit hex_digit hex_digit hex_digit hex_digit*  
  
 *clock-middle-value* ::= *hex_digit hex_digit hex_digit hex_digit*  
  
 *clock-high-value* ::= *hex_digit hex_digit hex_digit hex_digit*  
  
 *clock-seq-value* ::= *hex_digit hex_digit hex_digit hex_digit*  
  
 *clock-node-value* ::= *hex_digit hex_digit hex_digit hex_digit hex_digit hex_digit hex_digit hex_digit hex_digit hex_digit hex_digit hex_digit*  
  
 *hex_digit* ::= 0 &#124; 1 &#124; 2 &#124; 3 &#124; 4 &#124; 5 &#124; 6 &#124; 7 &#124; 8 &#124; 9 &#124; A &#124; B &#124; C &#124; D &#124; E &#124; F  
  
 The GUID literal escape sequence is supported if the GUID data type is supported by the data source. An application should call **SQLGetTypeInfo** to determine whether this data type is supported.