---
title: "Binding Parameters ODBC"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7538a82b-b08b-4c8f-9809-e4ccea16db11
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Binding Parameters ODBC
Each parameter in an SQL statement must be associated, or *bound,* to a variable in the application before the statement is executed. When the application binds a variable to a parameter, it describes that variable — address, C data type, and so on — to the driver. It also describes the parameter itself — SQL data type, precision, and so on. The driver stores this information in the structure it maintains for that statement and uses the information to retrieve the value from the variable when the statement is executed.  
  
 Parameters can be bound or rebound at any time before a statement is executed. If a parameter is rebound after a statement is executed, the binding does not apply until the statement is executed again. To bind a parameter to a different variable, an application simply rebinds the parameter with the new variable; the previous binding is automatically released.  
  
 A variable remains bound to a parameter until a different variable is bound to the parameter, until all parameters are unbound by calling **SQLFreeStmt** with the SQL_RESET_PARAMS option, or until the statement is released. For this reason, the application must be sure that variables are not freed until after they are unbound. For more information, see [Allocating and Freeing Buffers](../content/Allocating-and-Freeing-Buffers.md).  
  
 Because parameter bindings are just information stored in the structure maintained by the driver for the statement, they can be set in any order. They are also independent of the SQL statement that is executed. For example, suppose an application binds three parameters and then executes the following SQL statement:  
  
```  
INSERT INTO Parts (PartID, Description, Price) VALUES (?, ?, ?)  
```  
  
 If the application then immediately executes the SQL statement  
  
```  
SELECT * FROM Orders WHERE OrderID = ?, OpenDate = ?, Status = ?  
```  
  
 on the same statement handle, the parameter bindings for the **INSERT** statement are used because those are the bindings stored in the statement structure. In most cases, this is a poor programming practice and should be avoided. Instead, the application should call **SQLFreeStmt** with the SQL_RESET_PARAMS option to unbind all the old parameters and then bind new ones.  
  
 This section contains the following topics.  
  
-   [Binding Parameter Markers](../content/Binding-Parameter-Markers.md)  
  
-   [Binding Parameters by Name (Named Parameters)](../content/Binding-Parameters-by-Name--Named-Parameters-.md)  
  
-   [Parameter Binding Offsets](../content/Parameter-Binding-Offsets.md)  
  
-   [Describing Parameters](../content/Describing-Parameters.md)