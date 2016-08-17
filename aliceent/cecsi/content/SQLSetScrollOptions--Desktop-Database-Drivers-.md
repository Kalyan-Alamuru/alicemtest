---
title: "SQLSetScrollOptions (Desktop Database Drivers)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 51d643ed-015b-4639-969a-9491d9875aca
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLSetScrollOptions (Desktop Database Drivers)
Forward and static cursors are supported for SQL_CONCUR_READ_ONLY.  
  
 Only keyset-driven cursors are supported for an *fConcurrency* argument of SQL_CONCUR_LOCK.  
  
 An *fConcurrency* argument of SQL_CONCUR_ROWVER is not supported.  
  
 Dynamic cursors and mixed cursors are not supported.