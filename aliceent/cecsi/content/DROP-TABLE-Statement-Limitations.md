---
title: "DROP TABLE Statement Limitations"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0a1c80f5-c9f2-4655-9bfd-0131b2f015a9
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# DROP TABLE Statement Limitations
When the Microsoft Excel 5.0, 7.0, or 97 driver is used, the DROP TABLE statement clears the worksheet but does not delete the worksheet name. Because the worksheet name still exists in the workbook, another worksheet cannot be created with the same name.