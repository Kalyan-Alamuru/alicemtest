---
title: "Binding Columns"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c4407694-c8e1-4b0b-a39d-b007e6c3b54d
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Binding Columns
Data fetched from the data source is returned to the application in variables that the application has allocated for this purpose. Before this can be done, the application must associate, or *bind*, these variables to the columns of the result set; conceptually, this process is the same as binding application variables to statement parameters. When the application binds a variable to a result set column, it describes that variable — address, data type, and so on — to the driver. The driver stores this information in the structure it maintains for that statement and uses the information to return the value from the column when the row is fetched.  
  
 This section contains the following topics.  
  
-   [Binding Result Set Columns](../content/Binding-Result-Set-Columns.md)  
  
-   [Using SQLBindCol](../content/Using-SQLBindCol.md)