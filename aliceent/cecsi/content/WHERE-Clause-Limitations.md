---
title: "WHERE Clause Limitations"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 46b54f74-e4a3-4318-87cf-8a97c38a2718
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# WHERE Clause Limitations
The maximum number of clauses in a WHERE clause is 40.  
  
 LONGVARBINARY and LONGVARCHAR columns can be compared to literals of up to 255 characters in length, but cannot be compared using parameters.