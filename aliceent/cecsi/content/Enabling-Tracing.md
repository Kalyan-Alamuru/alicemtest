---
title: "Enabling Tracing"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 48e318bd-2487-4708-a698-ea01f36a45e9
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Enabling Tracing
Tracing can be enabled in the following three ways:  
  
-   Set the **Trace** and **TraceFile** keywords in the Odbc.ini registry entry. This enables or disables tracing when **SQLAllocHandle** with a *HandleType* of SQL_HANDLE_ENV is called. These options are set in the Tracing tab of the ODBC Data Source Administrator dialog box displayed during data source setup. For more information, see [Registry Entries for Data Sources](../content/Registry-Entries-for-Data-Sources.md).  
  
-   Call **SQLSetConnectAttr** to set the SQL_ATTR_TRACE connection attribute to SQL_OPT_TRACE_ON. This enables or disables tracing for the duration of the connection. For more information, see the [SQLSetConnectAttr](../content/SQLSetConnectAttr-Function.md) function description.  
  
-   Use **ODBCSharedTraceFlag** to turn tracing on or off dynamically. (For more information, see the next topic, [Dynamic Tracing](../content/Dynamic-Tracing.md).)