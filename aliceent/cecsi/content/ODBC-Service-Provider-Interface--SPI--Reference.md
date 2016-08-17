---
title: "ODBC Service Provider Interface (SPI) Reference"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cdeffb4a-f344-4abe-97f3-be2ede1c8e59
caps.latest.revision: 16
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# ODBC Service Provider Interface (SPI) Reference
Traditionally, ODBC defined an application programming interface (API). The functions in the API can be called by applications and they should be implemented inside both the Driver Manager and the driver.  
  
 With the addition of the driver-aware connection pooling feature, ODBC introduces the service provider interface (SPI). The functions in the SPI are used for communication between the Driver Manager and driver. SPI functions are implemented by the driver; the Driver Manager does not expose SPI functions to applications. Applications should not call these functions directly.  
  
 Include sqlspi.h for ODBC driver development.  
  
 This section contains the following topics  
  
-   [SQLCleanupConnectionPoolID](../content/SQLCleanupConnectionPoolID-Function.md)  
  
-   [SQLGetPoolID](../content/SQLGetPoolID-Function.md)  
  
-   [SQLPoolConnect](../content/SQLPoolConnect-Function.md)  
  
-   [SQLRateConnection](../content/SQLRateConnection-Function.md)  
  
-   [SQLSetConnectAttrForDbcInfo](../content/SQLSetConnectAttrForDbcInfo-Function.md)  
  
-   [SQLSetConnectInfo](../content/SQLSetConnectInfo-Function.md)  
  
-   [SQLSetDriverConnectInfo](../content/SQLSetDriverConnectInfo-Function.md)  
  
## See Also  
 [Developing an ODBC Driver](../content/Developing-an-ODBC-Driver.md)   
 [Developing Connection-Pool Awareness in an ODBC Driver](../content/Developing-Connection-Pool-Awareness-in-an-ODBC-Driver.md)   
 [Driver Manager Connection Pooling](../content/Driver-Manager-Connection-Pooling.md)