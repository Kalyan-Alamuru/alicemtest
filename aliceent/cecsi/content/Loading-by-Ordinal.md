---
title: "Loading by Ordinal"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 337d90ab-68eb-4940-a2f3-f7d5693ee766
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Loading by Ordinal
In ODBC 2.*x*, loading by ordinal could be performed to improve the performance of the connection process. An ODBC 2.*x* driver exports a dummy function with the ordinal 199; when the Driver Manager detects it, it resolves the addresses of the ODBC functions by ordinal, not by name. This functionality is still supported for ODBC 2.*x* drivers but is not supported for ODBC 3*.x* drivers.