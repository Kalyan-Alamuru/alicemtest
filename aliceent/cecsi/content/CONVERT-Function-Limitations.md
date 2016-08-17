---
title: "CONVERT Function Limitations"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3c81fc58-57f0-4dd7-be16-2b146eb15cbc
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# CONVERT Function Limitations
Type conversion failures result in the affected column being set to NULL.  
  
 Neither the DATE nor TIMESTAMP data type can be converted to another data type (or itself) by the CONVERT function.