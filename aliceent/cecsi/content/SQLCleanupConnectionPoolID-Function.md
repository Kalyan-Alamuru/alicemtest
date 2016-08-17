---
title: "SQLCleanupConnectionPoolID Function"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1fc61908-e003-4587-b91a-32f40569fb99
caps.latest.revision: 11
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLCleanupConnectionPoolID Function
**Conformance**  
 Version Introduced: ODBC 3.81 Standards Compliance: ODBC  
  
 **Summary**  
 **SQLCleanupConnectionPoolID** informs a driver that a pool ID was timed out. A pool ID can timeout whenever all connections in a pool associated with that pool ID were timed out. See [Pooling in the Microsoft Data Access Components](http://msdn.microsoft.com/library/ms810829.aspx) for more information about connection timeout.  
  
## Syntax  
  
```  
SQLRETURN  SQLCleanupConnectionPoolID (  
                SQLHENV    EnvironmentHandle  
                SQLPOOLID  PoolID );  
```  
  
## Arguments  
 *EnvironmentHandle*  
 [Input] The environment handle of the pool.  
  
 *PoolID*  
 [Input] The pool associated to the pool ID that was timed out.  
  
## Returns  
 SQL_SUCCESS, SQL_SUCCESS_WITH_INFO, SQL_ERROR, or SQL_INVALID_HANDLE.  
  
## Diagnostics  
 The Driver Manager will not process diagnostic information returned from **SQLCleanupConnectionPoolID**.  
  
 An application cannot receive the error message returned by the driver.  
  
## Remarks  
 **SQLCleanupConnectionPoolID** can be called at any time, but the Driver Manager guarantees that no other thread is simultaneously calling **SQLGetPoolID** and no other thread is simultaneously calling **SQLRateConnection** and **SQLPoolConnect** with a connection info token assigned with that pool ID. Therefore, the driver must make sure this function is thread safe.  
  
 A driver can clean up the resources associated with the pool ID.  
  
 Applications should not call this function directly. An ODBC driver that supports driver-aware connection pooling must implement this function.  
  
 Include sqlspi.h for ODBC driver development.  
  
## See Also  
 [Developing an ODBC Driver](../content/Developing-an-ODBC-Driver.md)   
 [Driver-Aware Connection Pooling](../content/Driver-Aware-Connection-Pooling.md)   
 [Developing Connection-Pool Awareness in an ODBC Driver](../content/Developing-Connection-Pool-Awareness-in-an-ODBC-Driver.md)