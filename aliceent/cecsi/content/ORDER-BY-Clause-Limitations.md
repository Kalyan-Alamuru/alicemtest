---
title: "ORDER BY Clause Limitations"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fd4ddc7c-9c7e-4a0c-a781-e5427dfb2e18
caps.latest.revision: 7
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# ORDER BY Clause Limitations
If a SELECT statement contains a GROUP BY clause and an ORDER BY clause, the ORDER BY clause can contain only a column in the result set or an expression in the GROUP BY clause.