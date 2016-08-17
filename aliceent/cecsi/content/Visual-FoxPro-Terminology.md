---
title: "Visual FoxPro Terminology"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a379b3cb-0393-46e7-b03b-724a56d8f31c
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Visual FoxPro Terminology
**database**  
 In Visual FoxPro, a database file has a .dbc extension and can contain one or more **tables**.  
  
 **database table**  
 In Visual FoxPro, a table that is associated with a database. Contrast **free table**.  
  
 **free table**  
 In Visual FoxPro, a table that is not associated with a database.  
  
 A .dbf file created in FoxPro version 2.x is a free table unless it is converted to a Visual FoxPro table and added to a Visual FoxPro database. Contrast **database table**.  
  
 **preparable SQL statement**  
 A SQL statement that has not already been processed by the **SQLPrepare** function. For more information about this function with the Visual FoxPro ODBC Driver, see [SQLPrepare (Visual FoxPro ODBC Driver)](../content/SQLPrepare--Visual-FoxPro-ODBC-Driver-.md).  
  
 **table**  
 In Visual FoxPro, records are stored in a table. Each row of a table represents a record, and the columns of the table represent the fields of the record. Each Visual FoxPro table is stored in its own file with a .dbf extension. Visual FoxPro tables can be associated with a database.  
  
 FoxPro version 2.*x* tables are not associated with a database.