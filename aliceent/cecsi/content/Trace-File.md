---
title: "Trace File"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ec97f949-126f-40a2-b67e-e74520a524cb
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Trace File
An application specifies the trace file either by setting the **TraceFile** keyword in the Odbc.ini registry entry or by calling **SQLSetConnectAttr** with the SQL_ATTR_TRACEFILE connection attribute. If the file does not exist when tracing is enabled, the Driver Manager will create the file. Each application should have its own dedicated trace file to avoid contention. An application can use more than one trace file; an application's setup program can provide the user with a choice of trace files. If tracing is enabled dynamically, an application can also display trace results, rather than logging to the trace file.  
  
 The trace file provides a log of each ODBC function call with the data types and values of all arguments. It logs all input functions and logs all returned functions with return codes and error states.  
  
 In ODBC 3*.x*, parameters to connection functions are not provided to the trace DLL.