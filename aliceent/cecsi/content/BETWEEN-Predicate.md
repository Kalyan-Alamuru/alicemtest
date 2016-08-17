---
title: "BETWEEN Predicate"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0cc7464b-d788-4720-98d8-411e1169185f
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# BETWEEN Predicate
The syntax:  
  
```  
expression1 BETWEEN expression2 AND expression3  
```  
  
 returns true only if *expression1* is greater than or equal to *expression2* and *expression1* is less than or equal to *expression3*.  
  
 The semantics of this syntax are different for the Desktop Database Drivers and the Microsoft Jet engine. In Microsoft Jet SQL, *expression2* can be greater than *expression3* so that the statement will return TRUE only if *expression1* is greater than or equal to *expression3*, and *expression1* is less than or equal to *expression2*.