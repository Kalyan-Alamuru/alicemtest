---
title: "INSERT - SQL Command"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9b648198-349f-46f6-b869-13d129945971
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# INSERT - SQL Command
Appends a record to the end of a table that contains the specified field values.  
  
 The Visual FoxPro ODBC Driver supports the native Visual FoxPro language syntax for this command. For driver-specific information, see the Remarks.  
  
## Syntax  
  
```  
  
INSERT INTO dbf_name [(fname1 [, fname2, ...])]  
   VALUES (eExpression1 [, eExpression2, ...])  
```  
  
## Arguments  
 INSERT INTO *dbf_name*  
 Specifies the name of the table to which the new record is appended. *dbf_name* can include a path and can be a name expression.  
  
 If the table you specify isn't open, it is opened exclusively in a new work area and the new record is appended to the table. The new work area isn't selected; the current work area remains selected.  
  
 If the table you specify is open, INSERT appends the new record to the table. If the table is open in a work area other than the current work area, it isn't selected after the record is appended; the current work area remains selected.  
  
 [( *fname1*[, *fname2*[, ...]])]  
 Specifies in the new record the names of the fields into which the values are inserted.  
  
 VALUES ( *eExpression1*[, *eExpression2*[, ...]])  
 Specifies the field values inserted into the new record. If you omit the field names, you must specify the field values in the order defined by the table structure.  
  
## Remarks  
 The new record contains the data listed in the VALUES clause.  
  
## Driver Remarks  
 When your application sends the ODBC SQL statement INSERT to the data source, the Visual FoxPro ODBC Driver converts the command into the Visual FoxProINSERT command without translation.  
  
## See Also  
 [CREATE TABLE - SQL Command](../content/CREATE-TABLE---SQL-Command.md)   
 [SELECT - SQL Command](../content/SELECT---SQL-Command.md)