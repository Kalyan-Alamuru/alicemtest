---
title: "SQLColAttributes (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d403dfa0-c26d-47d4-91d9-2f29aa387399
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLColAttributes (Visual FoxPro ODBC Driver)
> [!NOTE]  
>  This topic contains Visual FoxPro ODBC Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Support: Full  
  
 ODBC API Conformance: Core Level  
  
 Returns descriptor information for a column in a result set. Descriptor information is returned as a character string, a 32-bit descriptor-dependent value, or an integer value.  
  
> [!NOTE]  
>  **SQLColAttributes** cannot be used to return information about the bookmark column (column 0).  
  
 The Visual FoxPro ODBC Driver supports all *fDescType* values. The following table includes comments on the driver's implementation of selected values.  
  
|*fDescType*|Comment|  
|-----------------|-------------|  
|SQL_COLUMN_AUTO_INCREMENT|Returns FALSE: Visual FoxPro has no counter fields.|  
|SQL_COLUMN_CASE_SENSITIVE|Always returns TRUE if the column type is Character.|  
|SQL_COLUMN_LABEL|Returns the column name, which is also returned by SQL_COLUMN_NAME.|  
|SQL_COLUMN_MONEY|Returns TRUE if the column type is Currency (represented by a "Y" in the Visual FoxPro language).|  
|SQL_COLUMN_OWNER_NAME|Always returns an empty string.|  
|SQL_COLUMN_QUALIFIER_NAME|Always returns an empty string.|  
|SQL_COLUMN_SEARCHABLE|Returns SQL_UNSEARCHABLE for columns of type General; these columns cannot be used in a WHERE clause.<br /><br /> Returns SQL_SEARCHABLE for columns of type Character or Memo with NOCPTRANS not set; these columns can be used in a WHERE clause with any comparison operator.<br /><br /> Returns SQL_ALL_EXCEPT_LIKE for all other column types; these columns can be used in a WHERE clause with all comparison operators except LIKE.|  
|SQL_COLUMN_TABLE_NAME|Always returns an empty string.|  
  
 For more information, see [SQLColAttributes](../content/SQLColAttributes-Function.md) in the *ODBC Programmer's Reference*.