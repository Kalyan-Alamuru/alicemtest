---
title: "Tracing"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 77ed4c6c-d976-4eb2-8526-a12697b0ef83
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Tracing
The ODBC Driver Manager has a trace facility that allows the sequence of function calls made by an ODBC application to be recorded and transcribed into a log file. Tracing is performed by a trace DLL that captures calls between the application and the Driver Manager, and between the Driver Manager and the driver. This method of tracing replaces the tracing performed by the ODBC 2*.x* Driver Manager and the tracing performed in ODBC 2*.x* by ODBC Spy.  
  
 This section contains the following topics.  
  
-   [Trace DLL](../content/Trace-DLL.md)  
  
-   [Trace File](../content/Trace-File.md)  
  
-   [Enabling Tracing](../content/Enabling-Tracing.md)  
  
-   [Dynamic Tracing](../content/Dynamic-Tracing.md)