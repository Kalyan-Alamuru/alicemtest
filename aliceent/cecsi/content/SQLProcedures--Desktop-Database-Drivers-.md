---
title: "SQLProcedures (Desktop Database Drivers)"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c996ad6f-e790-40f4-a962-843422496149
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLProcedures (Desktop Database Drivers)
**SQLProcedures** will only return rows for those procedures that have at least one argument. Procedures that have no arguments are treated as views.  
  
|Column|Comments|  
|------------|--------------|  
|PROCEDURE_QUALIFIER|The path to the database file.|  
|PROCEDURE_OWNER|NULL|  
|PROCEDURE_NAME|Undelimited procedure name|  
|PROCEDURE_TYPE|SQL_PT_PROCEDURE|