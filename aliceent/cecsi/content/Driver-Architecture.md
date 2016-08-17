---
title: "Driver Architecture"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c5003413-0cc1-4f41-b877-a64e2f5ab118
caps.latest.revision: 7
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Driver Architecture
Driver architecture falls into two categories, depending on which software processes SQL statements:  
  
-   **File-Based Drivers** The driver accesses the physical data directly. In this case, the driver acts as both driver and data source; that is, it processes ODBC calls and SQL statements. For example, dBASE drivers are file-based drivers because dBASE does not provide a stand-alone database engine the driver can use. It is important to note that developers of file-based drivers must write their own database engines.  
  
-   **DBMS-Based Drivers** The driver accesses the physical data through a separate database engine. In this case the driver processes only ODBC calls; it passes SQL statements to the database engine for processing. For example, Oracle drivers are DBMS-based drivers because Oracle has a stand-alone database engine the driver uses. Where the database engine resides is immaterial. It can reside on the same machine as the driver or a different machine on the network; it might even be accessed through a gateway.  
  
 Driver architecture is generally interesting only to driver writers; that is, driver architecture generally makes no difference to the application. However, the architecture can affect whether an application can use DBMS-specific SQL. For example, Microsoft Access provides a stand-alone database engine. If a Microsoft Access driver is DBMS-based — it accesses the data through this engine — the application can pass Microsoft Access–SQL statements to the engine for processing.  
  
 However, if the driver is file-based — that is, it contains a proprietary engine that accesses the Microsoft® Access .mdb file directly — any attempts to pass Microsoft Access–specific SQL statements to the engine are likely to result in syntax errors. The reason is that the proprietary engine is likely to implement only ODBC SQL.  
  
 This section contains the following topics.  
  
-   [File-Based Drivers](../content/File-Based-Drivers.md)  
  
-   [DBMS-Based Drivers](../content/DBMS-Based-Drivers.md)  
  
-   [Network Example](../content/Network-Example.md)  
  
-   [Other Driver Architectures](../content/Other-Driver-Architectures.md)