---
title: "Date, Time, and Timestamp Escape Sequences"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 67b7dee0-e5b1-4469-a626-0c7767852b80
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Date, Time, and Timestamp Escape Sequences
ODBC defines escape sequences for date, time, and timestamp literals. The syntax of these escape sequences is as follows:  
  
```  
  
{d 'value'}  
{t 'value'}  
{ts 'value'}  
```  
  
 In BNF notation, the syntax is as follows:  
  
```  
  
      ODBC-date-time-escape ::=  
     ODBC-date-escape  
     | ODBC-time-escape  
     | ODBC-timestamp-escapeODBC-date-escape ::=  
     ODBC-esc-initiator d 'date-value' ODBC-esc-terminatorODBC-time-escape ::=  
     ODBC-esc-initiator t 'time-value' ODBC-esc-terminatorODBC-timestamp-escape ::=  
     ODBC-esc-initiator ts 'timestamp-value' ODBC-esc-terminatorODBC-esc-initiator ::= {  
ODBC-esc-terminator ::= }  
date-value ::=   
     years-value date-separator months-value date-separator days-valuetime-value ::=   
     hours-value time-separator minutes-value time-separatorseconds-valuetimestamp-value ::= date-value timestamp-separator time-valuedate-separator ::= -  
time-separator ::= :  
timestamp-separator ::=  
     (The blank character)years-value ::= digit digit digit digitmonths-value ::= digit digitdays-value ::= digit digithours-value ::= digit digitminutes-value ::= digit digitseconds-value ::= digit digit[.digit...]  
```  
  
## Remarks  
 The date, time, and timestamp literal escape sequences are supported if the date, time, and timestamp data types are supported by the data source. An application should call **SQLGetTypeInfo** to determine whether these data types are supported.