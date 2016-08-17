---
title: "Step 2: Initialize the Application"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 23a7a230-ae2c-4a5e-9760-d2e17f92c389
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Step 2: Initialize the Application
The second step is to initialize the application, as shown in the following illustration. Exactly what is done here varies with the application.  
  
 ![Shows initializing an ODBC application](../content/media/pr12.gif "pr12")  
  
 At this point, it is common to use **SQLGetInfo** to discover the capabilities of the driver. For more information, see [Considering Database Features to Use](../content/Considering-Database-Features-to-Use.md).  
  
 All applications need to allocate a statement handle with **SQLAllocHandle**, and many applications set statement attributes, such as the cursor type, with **SQLSetStmtAttr**. For more information, see [Allocating a Statement Handle](../content/Allocating-a-Statement-Handle-ODBC.md) and [Statement Attributes](../content/Statement-Attributes.md).