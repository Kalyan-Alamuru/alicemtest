---
title: "Multiple hstmts (Paradox Driver)"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 66aecd94-092d-43d4-9583-74f5e2990eac
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Multiple hstmts (Paradox Driver)
When the ODBC Paradox driver is used, if you want to use more than one *hstmt* to execute queries on a table, the table must have a unique index (Paradox primary key).