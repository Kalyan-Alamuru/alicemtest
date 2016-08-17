---
title: "SQLSetPos (Desktop Database Drivers)"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8ef027ec-8512-48fe-8fe2-2ff7cd81e331
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLSetPos (Desktop Database Drivers)
The bulk-model semantics for **SQLSetPos** calls with the *irow* argument equal to 0 are supported.  
  
 SQL_LOCK_NO_CHANGE is supported for *fLock*. SQL_LOCK_EXCLUSIVE and SQL_LOCK_UNLOCK are not supported.  
  
 **SQLSetPos** supports updatable joins. (For more information, see the *Microsoft Jet Database Engine Programmer's Guide*.)