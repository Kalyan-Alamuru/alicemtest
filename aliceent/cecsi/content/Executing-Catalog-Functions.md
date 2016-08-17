---
title: "Executing Catalog Functions"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c59cbda3-e214-4399-9edc-cfac86b378d7
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Executing Catalog Functions
Because a catalog function creates a result set, it is equivalent to executing any result set–generating SQL statement. In fact, catalog functions are often implemented by executing predefined SQL statements or calling predefined procedures that are shipped with the driver or DBMS. Almost anything that applies to SQL statements that create result sets also applies to catalog functions. For example, the SQL_ATTR_MAX_ROWS statement attribute limits the number of rows returned by the catalog function, just as it limits the number of rows returned by a **SELECT** statement.  
  
 To execute a catalog function, an application just calls the function.  
  
 For more information about catalog functions, see [Catalog Functions](../content/Catalog-Functions.md).