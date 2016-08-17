---
title: "Drivers"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d6795d92-877e-44e1-b7d5-2ff2fd3989bd
caps.latest.revision: 7
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Drivers
*Drivers* are libraries that implement the functions in the ODBC API. Each is specific to a particular DBMS; for example, a driver for Oracle cannot directly access data in an Informix DBMS. Drivers expose the capabilities of the underlying DBMSs; they are not required to implement capabilities not supported by the DBMS. For example, if the underlying DBMS does not support outer joins, then neither should the driver. The only major exception to this is that drivers for DBMSs that do not have stand-alone database engines, such as Xbase, must implement a database engine that at least supports a minimal amount of SQL.  
  
 This section contains the following topics.  
  
-   [Driver Tasks](../content/Driver-Tasks.md)  
  
-   [Driver Architecture](../content/Driver-Architecture.md)  
  
## See Also  
 [Microsoft-Supplied ODBC Drivers](../content/Microsoft-Supplied-ODBC-Drivers.md)