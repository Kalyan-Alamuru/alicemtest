---
title: "ODBC Driver Architecture"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 21a62c7c-192e-4718-a16e-aa12b0de4419
caps.latest.revision: 13
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# ODBC Driver Architecture
Driver writers must be aware that the driver architecture can affect whether an application can use DBMS-specific SQL.  
  
 ![Shows the ODBC driver architecture](../content/media/ODBCDriverOvruArch.gif "ODBCDriverOvruArch")  
  
 [File-based Drivers](../content/File-Based-Drivers.md)  
  
 When the driver accesses the physical data directly, the driver acts as both driver and data source. The driver must process both ODBC calls and SQL statements. Developers of file-based drivers must write their own database engines.  
  
 [DBMS-Based Drivers](../content/DBMS-Based-Drivers.md)  
  
 When a separate database engine is used to access physical data, the driver processes only ODBC calls. It passes SQL statements to the database engine for processing.  
  
 [Network Architecture](../content/Network-Example.md)  
  
 File and DBMS ODBC configurations can exist on a single network.  
  
 [Other Driver Architectures](../content/Other-Driver-Architectures.md)  
  
 When a driver is required to work with a variety of data sources, it can be used as middleware. Heterogeneous join engine architecture can make the driver appear as a driver manager. Drivers can also be installed on servers, where they can be shared by a series of clients.  
  
 For more information about driver architecture, see [Driver Manager](../content/The-Driver-Manager.md) and [Driver Architecture](../content/Driver-Architecture.md) in the section on [ODBC Architecture](../content/ODBC-Architecture.md).  
  
 More information about driver issues can be found in the locations described in the following table.  
  
|Issue|Topic|Location|  
|-----------|-----------|--------------|  
|Compatibility issues with applications and drivers|[Application/Driver Compatibility](../content/Application-and-Driver-Compatibility.md)|[Programming Considerations](../content/Programming-Considerations.md), in the ODBC Programmer's Reference|  
|Writing ODBC drivers|[Writing ODBC 3.x Drivers](../content/Writing-ODBC-3.x-Drivers.md)|[Programming Considerations](../content/Programming-Considerations.md), in the ODBC Programmer's Reference|  
|Driver guidelines for backward compatibility|[Driver Guidelines for Backward Compatibility](../Topic/Appendix%20G:%20Driver%20Guidelines%20for%20Backward%20Compatibility.md)|[Appendix G: Driver Guidelines for Backward Compatibility](../Topic/Appendix%20G:%20Driver%20Guidelines%20for%20Backward%20Compatibility.md), in the ODBC Programmer's Reference|  
|Connecting to a driver|[Choosing a Data Source or Driver](../content/Choosing-a-Data-Source-or-Driver.md)|[Connecting to a Data Source or Driver](../content/Connecting-to-a-Data-Source-or-Driver.md), in the ODBC Programmer's Reference|  
|Identifying drivers|[Viewing Drivers](../content/Viewing-Drivers.md)|[Viewing Drivers](../content/Viewing-Drivers.md), in the Microsoft ODBC Data Source Administrator online Help|  
|Enabling connection pooling|[ODBC Connection Pooling](../content/Driver-Manager-Connection-Pooling.md)|[Connecting to a Data Source or Driver](../content/Connecting-to-a-Data-Source-or-Driver.md), in the ODBC Programmer's Reference|  
|Unicode/ANSI driver and connection issues|[Unicode Drivers](../content/Unicode-Drivers.md)|[Programming Considerations](../content/Programming-Considerations.md), in the ODBC Programmer's Reference|  
  
## See Also  
 [Developing an ODBC Driver](../content/Developing-an-ODBC-Driver.md)