---
title: "ALTER TABLE Statement Limitations"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f3e88f85-edf4-47cd-a822-292b106ddb34
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# ALTER TABLE Statement Limitations
When the dBASE or Paradox driver is used, once an index has been created and a new record added, the structure of the table cannot be changed by the ALTER TABLE statement unless the index is dropped and the contents of the table are deleted.  
  
 ALTER TABLE statements are not supported for the Microsoft Excel or Text drivers.  
  
> [!NOTE]  
>  When you use the Paradox driver without implementing the Borland Database Engine, ALTER TABLE statements are not supported; only read and append statements are allowed.