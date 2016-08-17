---
title: "SQLTransact (Access Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 892b79c7-9e20-4d1f-bc60-d4b25694ca25
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLTransact (Access Driver)
> [!NOTE]  
>  This topic provides Access Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 When the Microsoft Access driver is used, SQL_COMMIT and SQL_ROLLBACK are supported for the *fType* argument in a call to **SQLTransact**.  
  
 If a failure occurs during the commit process, the affected database can be repaired using the Repair Database option in the Microsoft Access driver setup, or through the use of the REPAIR_DB keyword in the **SQLConfigDataSource** function.