---
title: "Arrays of Parameter Values"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9b572c5b-1dfe-40af-bebd-051548ab6d90
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Arrays of Parameter Values
It is often useful for applications to pass arrays of parameters. For example, using arrays of parameters and a parameterized **INSERT** statement, an application can insert a number of rows at once. There are several advantages to using arrays. First, network traffic is reduced because the data for many statements is sent in a single packet (if the data source supports parameter arrays natively). Second, some data sources can execute SQL statements using arrays faster than executing the same number of separate SQL statements. Finally, when the data is stored in an array, as is often the case for screen data, the application can bind all of the rows in a particular column with a single call to **SQLBindParameter** and update them by executing a single statement.  
  
 Unfortunately, not many data sources support parameter arrays. However, a driver can emulate parameter arrays by executing an SQL statement once for each set of parameter values. This can lead to increases in speed because the driver can then prepare the statement that it plans to execute once for each parameter set. It might also lead to simpler application code.  
  
 This section contains the following topics.  
  
-   [Binding Arrays of Parameters](../content/Binding-Arrays-of-Parameters.md)  
  
-   [Using Arrays of Parameters](../content/Using-Arrays-of-Parameters.md)