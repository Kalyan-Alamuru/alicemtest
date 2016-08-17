---
title: "ORDER BY expression-list"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5ef88186-a99f-4e2c-a3f3-98a42d4f03a5
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# ORDER BY expression-list
Expressions can be used in the ORDER BY clause. For example, in the following clauses the table is ordered by three key expressions: a+b, c+d, and e.  
  
```  
SELECT * FROM emp  
ORDER BY a+b,c+d,e  
```  
  
 No ordering is allowed on set functions or an expression that contains a set function.