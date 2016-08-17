---
title: "Driver Tasks"
ms.custom: na
ms.date: 08/03/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 184c795a-c2e8-4d20-9902-12e60b2f0e45
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Driver Tasks
Specific tasks performed by drivers include:  
  
-   Connecting to and disconnecting from the data source.  
  
-   Checking for function errors not checked by the Driver Manager.  
  
-   Initiating transactions; this is transparent to the application.  
  
-   Submitting SQL statements to the data source for execution. The driver must modify ODBC SQL to DBMS-specific SQL; this is often limited to replacing escape clauses defined by ODBC with DBMS-specific SQL.  
  
-   Sending data to and retrieving data from the data source, including converting data types as specified by the application.  
  
-   Mapping DBMS-specific errors to ODBC SQLSTATEs.