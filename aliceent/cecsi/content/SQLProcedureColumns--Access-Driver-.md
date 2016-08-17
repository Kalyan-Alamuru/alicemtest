---
title: "SQLProcedureColumns (Access Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 34fee995-5848-4ecb-bda0-fc362a77b2d9
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLProcedureColumns (Access Driver)
> [!NOTE]  
>  This topic provides Access Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Application developers should look for driver-defined columns starting at the end of the result set and proceeding backward.  
  
|Column|Comments|  
|------------|--------------|  
|COLUMN_TYPE|SQL_PARAM_INPUT or SQL_RESULT_COL|  
|ORDINAL|This is a driver-specific column that is returned at the end of the result set. The SQL type of the column is an integer.|