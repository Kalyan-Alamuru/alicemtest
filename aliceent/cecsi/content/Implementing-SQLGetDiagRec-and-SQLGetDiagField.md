---
title: "Implementing SQLGetDiagRec and SQLGetDiagField"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 11ba1857-b533-4517-8131-a2a8a0154a0a
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Implementing SQLGetDiagRec and SQLGetDiagField
**SQLGetDiagRec** and **SQLGetDiagField** are implemented by the Driver Manager and each driver. The Driver Manager and each driver maintain diagnostic records for each environment, connection, statement, and descriptor handle, and free those records only when another function is called with that handle or the handle is freed.  
  
 Although both the Driver Manager and each driver must determine the first status record according to the rankings in [Sequence of Status Records](../content/Sequence-of-Status-Records.md), the Driver Manager determines the final sequence of records.  
  
 **SQLGetDiagRec** and **SQLGetDiagField** do not post diagnostic records about themselves.  
  
 This section contains the following topics.  
  
-   [Diagnostic Handling Rules](../content/Diagnostic-Handling-Rules.md)  
  
-   [Role of the Driver Manager](../content/Role-of-the-Driver-Manager.md)  
  
-   [Role of the Driver](../content/Role-of-the-Driver.md)