---
title: "Step 3: Build and Execute an SQL Statement"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 133b8bd4-a3c8-4f7e-93c5-c05283c8e96f
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Step 3: Build and Execute an SQL Statement
The third step is to build and execute an SQL statement, as shown in the following illustration. The methods used to perform this step are likely to vary tremendously. The application might prompt the user to enter an SQL statement, build an SQL statement based on user input, or use a hard-coded SQL statement. For more information, see [Constructing SQL Statements](../content/Constructing-SQL-Statements.md).  
  
 ![Shows building and executing an SQL statement](../content/media/pr13.gif "pr13")  
  
 If the SQL statement contains parameters, the application binds them to application variables by calling **SQLBindParameter** for each parameter. For more information, see [Statement Parameters](../content/Statement-Parameters.md).  
  
 After the SQL statement is built and any parameters are bound, the statement is executed with **SQLExecDirect**. If the statement will be executed multiple times, it can be prepared with **SQLPrepare** and executed with **SQLExecute**. For more information, see [Executing a Statement](../content/Executing-a-Statement.md).  
  
 The application might also forgo executing an SQL statement altogether and instead call a function to return a result set containing catalog information, such as the available columns or tables. For more information, see [Uses of Catalog Data](../content/Uses-of-Catalog-Data.md).  
  
 The application's next action depends on the type of SQL statement executed.  
  
|Type of SQL statement|Proceed to|  
|---------------------------|----------------|  
|**SELECT** or catalog function|[Step 4a: Fetch the Results](../Topic/Step%204a:%20Fetch%20the%20Results.md)|  
|**UPDATE**, **DELETE**, or **INSERT**|[Step 4b: Fetch the Row Count](../Topic/Step%204b:%20Fetch%20the%20Row%20Count.md)|  
|All other SQL statements|Step 3: Build and Execute an SQL Statement (this topic) or [Step 5: Commit the Transaction](../Topic/Step%205:%20Commit%20the%20Transaction.md)|