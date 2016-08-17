---
title: "SQL_ARD_TYPE"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8d87ca10-f955-4284-8689-e9f4cc31e7ae
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQL_ARD_TYPE
The SQL_ARD_TYPE type identifier is used to indicate that the data in a buffer will be of the type specified in the SQL_DESC_CONCISE_TYPE field of the ARD. SQL_ARD_TYPE is entered in the *TargetType* argument of a call to **SQLGetData** instead of a specific data type and enables an application to change the data type of the buffer by changing the descriptor field. This value ties the data type of the *\*TargetValuePtr* buffer to the descriptor field. (SQL_ARD_TYPE is not entered in a call to **SQLBindCol** or **SQLBindParameter** because the type of the bound buffer is already tied to the SQL_DESC_TYPE and SQL_DESC_CONCISE_TYPE fields and can be changed at any time by changing either of those fields.)  
  
 The SQL_ARD_TYPE type identifier can be used to specify nondefault values for leading precision and seconds precision of interval data types, and precision and scale values for the SQL_C_NUMERIC data type. For more information, see [Overriding Default Leading and Seconds Precision for Interval Data Types](../content/Overriding-Default-Leading-and-Seconds-Precision-for-Interval-Data-Types.md) and [Overriding Default Precision and Scale for Numeric Data Types](../content/Overriding-Default-Precision-and-Scale-for-Numeric-Data-Types.md), later in this appendix.