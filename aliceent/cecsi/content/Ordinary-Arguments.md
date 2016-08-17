---
title: "Ordinary Arguments"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a18cdae1-6b85-41cb-875c-b5a01ec90aeb
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Ordinary Arguments
When a catalog function string argument is an ordinary argument, it is treated as a literal string. An ordinary argument accepts neither a string search pattern nor a list of values. The case of an ordinary argument is significant, and quote characters in the string are taken literally. These arguments are treated as ordinary arguments if the SQL_ATTR_METADATA_ID statement attribute is set to SQL_FALSE; they are treated as identifier arguments instead if this attribute is set to SQL_TRUE.  
  
 If an ordinary argument is set to a null pointer and the argument is a required argument, the function returns SQL_ERROR and SQLSTATE HY009 (Invalid use of null pointer). If an ordinary argument is set to a null pointer and the argument is not a required argument, the argument's behavior is driver-dependent. The required arguments are listed in the following table.  
  
|Function|Required arguments|  
|--------------|------------------------|  
|**SQLColumnPrivileges**|*TableName*|  
|**SQLForeignKeys**|*PKTableName*, *FKTableName*|  
|**SQLPrimaryKeys**|*TableName*|  
|**SQLSpecialColumns**|*TableName*|  
|**SQLStatistics**|*TableName*|