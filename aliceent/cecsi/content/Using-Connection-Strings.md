---
title: "Using Connection Strings"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 57634960-47e9-49bf-95c1-6e3702ac8166
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Using Connection Strings
You can use a connection string to connect to a Visual FoxPro data source.  
  
 For example, to connect to the TasTrade data source and override the current setting of Exclusive associated with the data source, you would use the string:  
  
```  
DSN=TasTrade;Exclusive=Yes  
```  
  
 For a list of the attribute keywords and values you can include in the connection string, see [SQLDriverConnect](../content/SQLDriverConnect--Visual-FoxPro-ODBC-Driver-.md).  
  
 For a complete explanation of connection string syntax, see [SQLBrowseConnect](../content/SQLBrowseConnect-Function.md) in the *ODBC Programmer's Reference*.