---
title: "Environment Handles"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 917f1b0c-272b-4e37-a1f5-87cd24b9fa21
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Environment Handles
An *environment* is a global context in which to access data; associated with an environment is any information that is global in nature, such as:  
  
-   The environment's state  
  
-   The current environment-level diagnostics  
  
-   The handles of connections currently allocated on the environment  
  
-   The current settings of each environment attribute  
  
 Within a piece of code that implements ODBC (the Driver Manager or a driver), an environment handle identifies a structure to contain this information.  
  
 Environment handles are not frequently used in ODBC applications. They are always used in calls to **SQLDataSources** and **SQLDrivers** and sometimes used in calls to **SQLAllocHandle**, **SQLEndTran**, **SQLFreeHandle**, **SQLGetDiagField**, and **SQLGetDiagRec**.  
  
 Each piece of code that implements ODBC (the Driver Manager or a driver) contains one or more environment handles. For example, the Driver Manager maintains a separate environment handle for each application that is connected to it. Environment handles are allocated with **SQLAllocHandle** and freed with **SQLFreeHandle**.