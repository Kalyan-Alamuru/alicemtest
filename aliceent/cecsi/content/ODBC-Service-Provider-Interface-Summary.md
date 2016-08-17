---
title: "ODBC Service Provider Interface Summary"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ace6085b-355b-435b-8734-503fc3c12ec2
caps.latest.revision: 4
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# ODBC Service Provider Interface Summary
The following table describes ODBC Service Provider interface functions. For more information about the syntax and semantics for each function, see [ODBC Service Provider Interface (SPI) Reference](../content/ODBC-Service-Provider-Interface--SPI--Reference.md).  
  
|Function name|Purpose|  
|-------------------|-------------|  
|[SQLSetConnectAttrForDbcInfo](../content/SQLDataSourceToDriver-Function.md)|Same as [SQLSetConnectAttr](../content/SQLSetConnectAttr-Function.md), but it sets the attribute on the connection information token instead of on the connection handle.|  
|[SQLSetDriverConnectInfo](../content/SQLDriverToDataSource-Function.md)|Sets the connection string into the connection info token for an application’s [SQLDriverConnect](../content/SQLDriverConnect-Function.md) call.|  
|[SQLSetConnectInfo](../content/SQLDataSourceToDriver-Function.md)|Sets the data source, user ID, and password into the connection info token for an application’s [SQLConnect](../content/SQLConnect-Function.md) call.|  
|[SQLGetPoolID](../content/SQLDataSourceToDriver-Function.md)|Retrieves the pool ID.|  
|[SQLRateConnection](../content/SQLDataSourceToDriver-Function.md)|Determines if a driver can reuse an existing connection in the connection pool.|  
|[SQLPoolConnect](../content/SQLDataSourceToDriver-Function.md)|Create a new connection if no connection in the pool can be reused.|  
|[SQLCleanupConnectionPoolID](../content/SQLDataSourceToDriver-Function.md)|Informs a driver that a pool ID was timed out.|