---
title: "Supported Concurrency Model (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c39ed963-3af1-4888-8631-6083692ddcd7
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Supported Concurrency Model (Visual FoxPro ODBC Driver)
The Visual FoxPro ODBC Driver supports *read-only concurrency*. Your application can call [SQLSetStmtOption](../content/SQLSetStmtOption--Visual-FoxPro-ODBC-Driver-.md) with a SQL_CONCURRENCY option of SQL_CONCUR_READ_ONLY.  
  
 For more information, see the [ODBC Programmer's Reference](../content/ODBC-Programmer-s-Reference.md).  
  
## read-only concurrency  
 The cursor cannot be updated.  
  
## row versioning  
 Essentially timestamp support, in which row versions are compared at update time.