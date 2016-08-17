---
title: "CString Class"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 18630642-76fa-43c4-a154-3f0969ec9b50
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# CString Class
Because objects of the **CString** class in Microsoft® Visual C++® are signed and string arguments in ODBC functions are unsigned, applications that pass **CString** objects to ODBC functions without casting them will receive compiler warnings.