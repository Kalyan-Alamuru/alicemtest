---
title: "Connection Strings"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 724c7b86-300a-4fa9-ad96-4afa0fdcb3e9
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Connection Strings
A connection string contains information used for establishing a connection. A complete connection string contains all the information needed to establish a connection. The connection string is a series of keyword/value pairs separated by semicolons. (For the complete syntax of a connection string, see the [SQLDriverConnect](../content/SQLDriverConnect-Function.md) function description.) The connection string is used by:  
  
-   **SQLDriverConnect**, which completes the connection string by interaction with the user.  
  
-   **SQLBrowseConnect**, which completes the connection string iteratively with the data source.  
  
 **SQLConnect** does not use a connection string; using **SQLConnect** is analogous to connecting using a connection string with exactly three keyword/value pairs (for data source name and, optionally, user ID and password).