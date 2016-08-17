---
title: "Step 6: Disconnect from the Data Source"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6ad759ba-4721-4d8f-9b26-de976d4fc1a0
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Step 6: Disconnect from the Data Source
The final step is to disconnect from the data source, as shown in the following illustration. First, the application frees any statement handles by calling **SQLFreeHandle**. For more information, see [Freeing a Statement Handle](../content/Freeing-a-Statement-Handle-ODBC.md).  
  
 ![Shows disconnecting from a data source](../content/media/pr17.gif "pr17")  
  
 Next, the application disconnects from the data source with **SQLDisconnect** and frees the connection handle with **SQLFreeHandle**. For more information, see [Disconnecting from a Data Source or Driver](../content/Disconnecting-from-a-Data-Source-or-Driver.md).  
  
 Finally, the application frees the environment handle with **SQLFreeHandle** and unloads the Driver Manager. For more information, see [Allocating the Environment Handle](../content/Allocating-the-Environment-Handle.md).