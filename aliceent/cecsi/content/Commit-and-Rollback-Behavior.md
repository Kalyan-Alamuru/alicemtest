---
title: "Commit and Rollback Behavior"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2ac8f012-e46d-41ca-81bb-e4a3246e3241
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Commit and Rollback Behavior
A common behavior among server DBMSs is to close cursors and discard prepared statements when a statement is committed or rolled back. Desktop databases are more likely to keep cursors open and keep prepared statements. For more information, see the SQL_CURSOR_COMMIT_BEHAVIOR and SQL_CURSOR_ROLLBACK_BEHAVIOR options in the [SQLGetInfo](../content/SQLGetInfo-Function.md) function description and [Effect of Transactions on Cursors and Prepared Statements](../content/Effect-of-Transactions-on-Cursors-and-Prepared-Statements.md).