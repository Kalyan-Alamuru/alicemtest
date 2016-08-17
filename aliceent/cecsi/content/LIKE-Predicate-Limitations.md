---
title: "LIKE Predicate Limitations"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dbd39099-caf6-4c4c-9ad8-f6c63c1bd5e4
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# LIKE Predicate Limitations
If data in a column is longer than 255 characters, the LIKE comparison will be based only on the first 255 characters.  
  
 A LIKE used in a procedure is supported only with constant patterns. The Desktop Database Drivers support SQL-92 LIKE pattern matching.  
  
 Use of an escape clause in a LIKE predicate is not supported.  
  
 A LIKE comparison should not be performed on a column containing data of a numeric or float data type. The results may be unpredictable. For more information, see the *Microsoft Jet Database Engine Programmer's Guide*.