---
title: "SQLSpecialColumns (Desktop Database Drivers)"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3de66fdf-053b-4354-979d-e76a5a5e975f
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLSpecialColumns (Desktop Database Drivers)
A unique index will be returned (if one exists) for the SQL_BEST_ROWID flag in *fColType*. No result set will be returned for the SQL_ROWVER flag.  
  
 All row IDs have a scope of SQL_SCOPE_CURROW.  
  
 Pattern matching is not supported for either the *szTableQualifier* or *szTableName* argument.