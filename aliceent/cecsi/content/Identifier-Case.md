---
title: "Identifier Case"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ee8a31aa-389d-4dd1-bfa9-547f6b50bc70
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Identifier Case
In SQL statements and catalog function arguments, identifiers and quoted identifiers can be either case-sensitive or not, which an application can determine by calling **SQLGetInfo** with the SQL_IDENTIFIER_CASE and SQL_QUOTED_IDENTIFIER_CASE options.  
  
 Each of these options has four possible return values: one stating that the identifier or quoted identifier case is sensitive and three stating that it is not sensitive. The three values that are not case-sensitive further describe the case in which identifiers are stored in the system catalog. How identifiers are stored in the system catalog is relevant only for display purposes, such as when an application displays the results of a catalog function; it does not change the case-sensitivity of identifiers.