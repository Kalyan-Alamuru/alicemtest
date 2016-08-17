---
title: "DELETE Statement Limitations"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 084761fe-e65b-4f38-ba4f-69884b2a7700
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# DELETE Statement Limitations
The DELETE statement is not supported for the Microsoft Excel or Text driver. Note that the INSERT statement is supported for the Text driver.  
  
 The dBASE driver does not support packing a table to remove "deleted" values.  
  
 For the Paradox driver to delete a row from a table, the table must have a unique index (Paradox primary key).