---
title: "SQLGetDescField and SQLGetDescRec (Cursor Library)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1a801f22-6fea-48aa-a723-3187a2ad852b
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLGetDescField and SQLGetDescRec (Cursor Library)
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work and plan to modify applications that currently use this feature. Microsoft recommends using the driver's cursor functionality.  
  
 This topic discusses the use of the **SQLGetDescField** and **SQLGetDescRec** functions in the cursor library. For general information about these functions, see [SQLGetDescField Function](../content/SQLGetDescField-Function.md) and [SQLGetDescRec Function](../content/SQLGetDescRec-Function.md).  
  
 The cursor library executes **SQLGetDescRec** to return metadata for bookmark columns. The cursor library executes **SQLGetDescField** to return the same fields returned by **SQLGetDescRec**, which are SQL_DESC_NAME, SQL_DESC_TYPE, SQL_DESC_DATETIME_INTERVAL_CODE, SQL_DESC_OCTET_LENGTH, SQL_DESC_PRECISION, SQL_DESC_SCALE, and SQL_DESC_NULLABLE. For consistency, **SQLGetDescField** also returns SQL_DESC_UNNAMED.  
  
 The cursor library executes **SQLGetDescField** when it is called to return the value of the following fields that are set for binding bookmark columns: SQL_DESC_DATA_PTR, SQL_DESC_INDICATOR_PTR, SQL_DESC_OCTET_LENGTH_PTR, and SQL_DESC_LENGTH.  
  
 The cursor library executes **SQLGetDescField** when it is called to return the value of the SQL_DESC_BIND_OFFSET_PTR, SQL_DESC_BIND_TYPE, SQL_DESC_ROW_ARRAY_SIZE, or SQL_DESC_ROW_STATUS_PTR field. These fields can be returned for any row, not just the bookmark row.  
  
 If an application calls **SQLGetDescField** to return the value of any field other than those mentioned previously, the cursor library passes the call to the driver.