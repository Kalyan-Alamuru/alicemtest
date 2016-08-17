---
title: "Escape Sequences in ODBC"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cf229f21-6c38-4b5b-aca8-f1be0dfeb3d0
caps.latest.revision: 7
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Escape Sequences in ODBC
A number of language features, such as outer joins and scalar function calls, are commonly implemented by DBMSs. However, the syntaxes for these features tend to be DBMS-specific, even when standard syntaxes are defined by the various standards bodies. Because of this, ODBC defines escape sequences that contain standard syntaxes for the following language features:  
  
-   Date, time, timestamp, and datetime interval literals  
  
-   Scalar functions such as numeric, string, and data type conversion functions  
  
-   LIKE predicate escape character  
  
-   Outer joins  
  
-   Procedure calls  
  
 The escape sequence used by ODBC is as follows:  
  
```  
  
(extension)  
  
```  
  
## Remarks  
 The escape sequence is recognized and parsed by drivers, which replace the escape sequences with DBMS-specific grammar. For more information about escape sequence syntax, see [ODBC Escape Sequences](../content/ODBC-Escape-Sequences.md) in Appendix C: SQL Grammar.  
  
> [!NOTE]  
>  In ODBC 2.*x*, this was the standard syntax of the escape sequence:            **--(\*vendor(***vendor-name***), product(***product-name***)***extension* **\*)--**  
>   
>  In addition to this syntax, a shorthand syntax was defined of the form:            **{***extension***}**  
>   
>  In ODBC 3.*x*, the long form of the escape sequence has been deprecated, and the shorthand form is used exclusively.  
  
 Because the escape sequences are mapped by the driver to DBMS-specific syntaxes, an application can use either the escape sequence or DBMS-specific syntax. However, applications that use the DBMS-specific syntax will not be interoperable. When using the escape sequence, applications should make sure that the SQL_ATTR_NOSCAN statement attribute is turned off, which it is by default. Otherwise, the escape sequence will be sent directly to the data source, where it will generally cause a syntax error.  
  
 Drivers support only those escape sequences that they can map to underlying language features. For example, if the data source does not support outer joins, neither will the driver. To determine which escape sequences are supported, an application calls **SQLGetTypeInfo** and **SQLGetInfo**. For more information, see the next section, [Date, Time, and Timestamp Literals](../content/Date--Time--and-Timestamp-Literals.md).  
  
 This section contains the following topics.  
  
-   [Date, Time, and Timestamp Literals](../content/Date--Time--and-Timestamp-Literals.md)  
  
-   [Scalar Function Calls](../content/Scalar-Function-Calls.md)  
  
-   [LIKE Predicate Escape Character](../content/LIKE-Predicate-Escape-Character.md)  
  
-   [Outer Joins](../content/Outer-Joins.md)  
  
-   [Procedure Calls](../content/Procedure-Calls.md)