---
title: "Step 5: Commit the Transaction"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 311685e2-f7b5-4ddc-8020-59380cd2f035
caps.latest.revision: 7
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Step 5: Commit the Transaction
The next step is to commit the transaction, as shown in the following illustration.  
  
 ![Shows how to commit a transaction](../content/media/pr16.gif "pr16")  
  
 The fifth step is to call **SQLEndTran** to commit or roll back the transaction. The application performs this step only if it set the transaction commit mode to manual-commit; if the transaction commit mode is auto-commit, which is the default, the transaction is automatically committed when the statement is executed. For more information, see [Transactions](../content/Transactions-ODBC.md).  
  
 To execute a statement in a new transaction, the application returns to step 3. To disconnect from the data source, the application proceeds to step 6.