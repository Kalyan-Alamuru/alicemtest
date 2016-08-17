---
title: "Multiple Active Statements and Connections"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a6571356-b23e-4f10-a17b-bce09460b71e
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Multiple Active Statements and Connections
Some drivers and DBMSs limit the number of statements and connections that can be active at one time. These numbers can be as small as one. For more information, see the SQL_MAX_CONCURRENT_ACTIVITIES and SQL_MAX_DRIVER_CONNECTIONS options in the [SQLGetInfo](../content/SQLGetInfo-Function.md) function description, and [Statement Handles](../content/Statement-Handles.md) and [Connection Handles](../content/Connection-Handles.md).