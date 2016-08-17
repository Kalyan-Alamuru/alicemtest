---
title: "Using Data Type Identifiers"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 467e0c0c-a818-4737-8a24-3d8e15c7e162
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Using Data Type Identifiers
Applications use data type identifiers in two ways: to describe their buffers to the driver, and to retrieve metadata about the result set from the driver so that they can determine what type of C buffers to use to store the data. Applications call the following functions to perform these tasks:  
  
-   **SQLBindParameter**, **SQLBindCol**, and **SQLGetData** — to describe the C data type of application buffers.  
  
-   **SQLBindParameter** — to describe the SQL data type of dynamic parameters.  
  
-   **SQLColAttribute** and **SQLDescribeCol** — to retrieve the SQL data types of result set columns.  
  
-   **SQLDescribeParameter** — to retrieve the SQL data types of parameters.  
  
-   **SQLColumns**, **SQLProcedureColumns**, and **SQLSpecialColumns** — to retrieve the SQL data types of various schema information  
  
-   **SQLGetTypeInfo** — to retrieve a list of supported data types  
  
 Data type identifiers are stored in the SQL_DESC_CONCISE_TYPE field of a descriptor. The descriptor functions **SQLSetDescField** and **SQLSetDescRec** can be used with the appropriate types to perform the tasks listed in the previous list. For more information, see [SQLSetDescField](../content/SQLSetDescField-Function.md).