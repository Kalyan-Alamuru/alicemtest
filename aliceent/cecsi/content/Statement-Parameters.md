---
title: "Statement Parameters"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 58d5b166-2578-4699-a560-1f1e6d86c49a
caps.latest.revision: 7
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Statement Parameters
A *parameter* is a variable in an SQL statement. For example, suppose a Parts table has columns named PartID, Description, and Price. To add a part without parameters would require constructing an SQL statement such as:  
  
```  
INSERT INTO Parts (PartID, Description, Price) VALUES (2100, 'Drive shaft', 50.00)  
```  
  
 Although this statement inserts a new order, it is not a good solution for an order entry application because the values to insert cannot be hard-coded in the application. An alternative is to construct the SQL statement at run time, using the values to be inserted. This is also not a good solution, because of the complexity of constructing statements at run time. The best solution is to replace the elements of the **VALUES** clause with question marks (?), or *parameter markers*:  
  
```  
INSERT INTO Parts (PartID, Description, Price) VALUES (?, ?, ?)  
```  
  
 The parameter markers are then bound to application variables. To add a new row, the application has only to set the values of the variables and execute the statement. The driver then retrieves the current values of the variables and sends them to the data source. If the statement will be executed multiple times, the application can make the process even more efficient by preparing the statement.  
  
 The statement just shown might be hard-coded in an order entry application to insert a new row. However, parameter markers are not limited to vertical applications. For any application, they ease the difficulty of constructing SQL statements at run time by avoiding conversions to and from text. For example, the part ID just shown is most likely stored in the application as an integer. If the SQL statement is constructed without parameter markers, the application must convert the part ID to text and the data source must convert it back to an integer. By using a parameter marker, the application can send the part ID to the driver as an integer, which usually can send it to the data source as an integer. This saves two conversions. For long data values, this is very important, because the text forms of such values frequently exceed the allowed length of an SQL statement.  
  
 Parameters are valid only in certain places in SQL statements. For example, they are not allowed in the select list (the list of columns to be returned by a **SELECT** statement), nor are they allowed as both operands of a binary operator such as the equal sign (=), because it would be impossible to determine the parameter type. Generally, parameters are valid only in Data Manipulation Language (DML) statements, and not in Data Definition Language (DDL) statements. For more information, see [Parameter Markers](../content/Parameter-Markers.md) in Appendix C: SQL Grammar.  
  
 When the SQL statement invokes a procedure, named parameters can be used. Named parameters are identified by their names, not by their position in the SQL statement. They can be bound by a call to **SQLBindParameter**, but the parameter is identified by the SQL_DESC_NAME field of the IPD (implementation parameter descriptor), not by the *ParameterNumber* argument of **SQLBindParameter**. They can also be bound by calling **SQLSetDescField** or **SQLSetDescRec**. For more information about named parameters, see [Binding Parameters by Name (Named Parameters)](../content/Binding-Parameters-by-Name--Named-Parameters-.md), later in this section. For more information about descriptors, see [Descriptors](../content/Descriptors.md).  
  
 This section contains the following topics.  
  
-   [Binding Parameters](../content/Binding-Parameters-ODBC.md)  
  
-   [Setting Parameter Values](../content/Setting-Parameter-Values.md)  
  
-   [Sending Long Data](../content/Sending-Long-Data.md)  
  
-   [Retrieving Output Parameters by SQLGetData](../content/Retrieving-Output-Parameters-Using-SQLGetData.md)  
  
-   [Procedure Parameters](../content/Procedure-Parameters.md)  
  
-   [Arrays of Parameter Values](../content/Arrays-of-Parameter-Values.md)