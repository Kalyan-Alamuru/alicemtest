---
title: "Step 4b: Fetch the Row Count"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3af481b1-d694-446e-948d-e3a5edcad050
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Step 4b: Fetch the Row Count
The next step is to fetch the row count, as shown in the following illustration.  
  
 ![Shows fetching the row count](../content/media/pr15.gif "pr15")  
  
 If the statement executed in Step 3 was an **UPDATE**, **DELETE**, or **INSERT** statement, the application retrieves the count of affected rows with **SQLRowCount**. For more information, see [Determining the Number of Affected Rows](../content/Determining-the-Number-of-Affected-Rows.md).  
  
 The application now returns to step 3 to execute another statement in the same transaction or proceeds to step 5 to commit or roll back the transaction.