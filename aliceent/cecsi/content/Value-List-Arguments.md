---
title: "Value List Arguments"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 863837be-603b-4c7a-8b96-b71014037ee5
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Value List Arguments
A value list argument consists of a list of comma-separated values to be used for matching. There is only one value list argument in the ODBC catalog functions: the *TableType* argument in **SQLTables**. Setting *TableType* to a null pointer is the same as if it is set to SQL_ALL_TABLE_TYPES, which enumerates all possible members of the value list. This argument is not affected by the SQL_ATTR_METADATA_ID statement attribute. For more information, see the [SQLTables](../content/SQLTables-Function.md) function description.