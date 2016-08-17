---
title: "Manual-Commit Mode"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9c4b3931-e48b-4960-89a2-5697537e9f51
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Manual-Commit Mode
*In manual-commit mode,* applications must explicitly complete transactions by calling **SQLEndTran** to commit them or roll them back. This is the normal transaction mode for most relational databases.  
  
 Transactions in ODBC do not have to be explicitly initiated. Instead, a transaction begins implicitly whenever the application starts operating on the database. If the data source requires explicit transaction initiation, the driver must provide it whenever the application executes a statement requiring a transaction and there is no current transaction.