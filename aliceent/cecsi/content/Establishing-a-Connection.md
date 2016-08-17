---
title: "Establishing a Connection"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8e3c717e-35e3-47ef-b5d3-3a96eeb7b869
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Establishing a Connection
After allocating environment and connection handles and setting any connection attributes, the application is ready to connect to the data source or driver. There are three different functions the application can use to do this: **SQLConnect** (Core interface conformance level), **SQLDriverConnect** (Core), and **SQLBrowseConnect** (Level 1). Each of the three is designed to be used in a different scenario. Before connecting, the application can determine which of these functions is supported with the **ConnectFunctions** keyword returned by **SQLDrivers**.  
  
> [!NOTE]  
>  Some drivers limit the number of active connections they support. An application calls **SQLGetInfo** with the SQL_MAX_DRIVER_CONNECTIONS option to determine how many active connections a particular driver supports.  
  
 This section contains the following topics.  
  
-   [Default Data Source](../content/Default-Data-Source.md)  
  
-   [Connecting with SQLConnect](../content/Connecting-with-SQLConnect.md)  
  
-   [Connection Strings](../content/Connection-Strings.md)  
  
-   [Connecting with SQLDriverConnect](../content/Connecting-with-SQLDriverConnect.md)  
  
-   [Connecting with SQLBrowseConnect](../content/Connecting-with-SQLBrowseConnect.md)