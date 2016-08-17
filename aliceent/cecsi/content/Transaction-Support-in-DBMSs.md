---
title: "Transaction Support in DBMSs"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0fc2ae34-4748-4120-9fc3-bb28c8ed867e
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Transaction Support in DBMSs
Some databases, especially desktop databases such as dBASE, Paradox, and Btrieve, do not support transactions. Even among databases that support transactions, there is variation in what kinds of SQL statements can be in a transaction. For more information, see the SQL_TXN_CAPABLE option in the [SQLGetInfo](../content/SQLGetInfo-Function.md) function description.