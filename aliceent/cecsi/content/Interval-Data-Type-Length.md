---
title: "Interval Data Type Length"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e9eb38d8-f9db-4401-8c62-aa394054cbbf
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Interval Data Type Length
The following rules are used to determine the length of an interval data type in characters. Length is expressed in number of characters. The number of bytes depends upon the character set. The length includes the following values added together:  
  
-   Two characters for every field in the interval that is not the leading field.  
  
-   For the leading field, the number of characters that is the express or implicit leading precision. If the leading precision is not specified, the default value is 2.  
  
-   One character for the separator between the fields.  
  
-   One plus the express or implied seconds precision. If the seconds precision is not specified, the default value is 6.  
  
 Specific column length values for each interval data type are contained in [Column Size](../content/Column-Size.md).