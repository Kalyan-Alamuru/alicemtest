---
title: "Supported ODBC API Functions"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b28a8ed6-09b1-4acf-bf3e-f90bb32422de
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Supported ODBC API Functions
The purpose of leveling is to inform the application what features are available to it from the driver. The Microsoft ODBC Desktop Database Drivers support all Core and Level 1 functions.  
  
 For more information about conformance levels for functions and grammar, see [Conformance Levels](../content/Conformance-Levels.md) in the *ODBC Programmer's Reference*.  
  
 Support of ODBC API functions can be dependent on the driver used. The following table summarizes the support for functions. The leftmost column provides a link to the general reference page for each function. These reference pages are listed alphabetically in the [ODBC API Reference](../content/ODBC-API-Reference.md) section, under [ODBC Programmer's Reference](../content/ODBC-Programmer-s-Reference.md). The columns to the right provide links to driver-specific notes about each supported function. These driver-specific topics are listed in the "Other Programming Details" section for each driver. Alternatively, if the same remarks about a function apply to all the ODBC Desktop Database Drivers, the rightmost column provides a link to a topic that summarizes the Desktop Database Drivers' support for that function. These topics are listed at the end of the current section ("Supported ODBC API Functions").  
  
|ODBC Function|Access Driver-specific notes|dBASE Driver-specific notes|Paradox Driver-specific notes|Text File Driver-specific notes|Excel Driver-specific notes|Notes relevant to all drivers|  
|-------------------|-----------------------------------|----------------------------------|------------------------------------|--------------------------------------|----------------------------------|-----------------------------------|  
|[SQLBindParameter](../content/SQLBindParameter-Function.md)|||||[Excel](../content/SQLBindParameter--Excel-Driver-.md)||  
|[SQLColAttributes](../content/SQLColAttributes-Function.md)|[Access](../content/SQLColAttributes--Access-Driver-.md)|[dBASE](../content/SQLColAttributes--dBASE-Driver-.md)|[Paradox](../content/SQLColAttributes--Paradox-Driver-.md)|[Text File](../content/SQLColAttributes--Text-File-Driver-.md)|[Excel](../content/SQLColAttributes--Excel-Driver-.md)||  
|[SQLColumns](../content/SQLColAttributes-Function.md)|[Access](../content/SQLColAttributes--Access-Driver-.md)|[dBASE](../content/SQLColAttributes--dBASE-Driver-.md)|[Paradox](../content/SQLColAttributes--Paradox-Driver-.md)|[Text File](../content/SQLColAttributes--Text-File-Driver-.md)|[Excel](../content/SQLColAttributes--Excel-Driver-.md)||  
|[SQLConfigDataSource](../content/SQLConfigDataSource-Function.md)|[Access](../content/SQLConfigDataSource--Access-Driver-.md)|[dBASE](../content/SQLConfigDataSource--dBASE-Driver-.md)|[Paradox](../content/SQLConfigDataSource--Paradox-Driver-.md)|[Text File](../content/SQLConfigDataSource--Text-File-Driver-.md)|[Excel](../content/ODBC-Jet-SQLConfigDataSource--Excel-Driver-.md)||  
|[SQLDriverConnect](../content/SQLDriverConnect-Function.md)|[Access](../content/SQLDriverConnect--Access-Driver-.md)|[dBASE](../content/SQLDriverConnect--dBASE-Driver-.md)|[Paradox](../content/SQLDriverConnect--Paradox-Driver-.md)|[Text File](../content/SQLDriverConnect--Text-File-Driver-.md)|[Excel](../content/SQLDriverConnect--Excel-Driver-.md)||  
|[SQLGetCursorName](../content/SQLGetCursorName-Function.md)||||||[All drivers](../content/SQLGetCursorName--Desktop-Database-Drivers-.md)|  
|[SQLGetData](../content/SQLGetData-Function.md)||||||[All drivers](../content/SQLGetData--Desktop-Database-Drivers-.md)|  
|[SQLGetInfo](../content/SQLGetInfo-Function.md)|[Access](../content/SQLGetInfo--Access-Driver-.md)|[dBASE](../content/SQLGetInfo--dBASE-Driver-.md)|[Paradox](../content/SQLGetInfo--Paradox-Driver-.md)|[Text File](../content/SQLGetInfo--Text-File-Driver-.md)|[Excel](../content/SQLGetInfo--Excel-Driver-.md)||  
GetStmtOption](../Topic/SQLGetStmtOption%20Function.md)|[All drivers](../content/SQLGetStmtOption--Desktop-Database-Drivers-.md)||||||  
|[SQLGetTypeInfo](../content/SQLGetTypeInfo-Function.md)|[Access](../content/SQLGetTypeInfo--Access-Driver-.md)|[dBASE](../content/SQLGetTypeInfo--dBASE-Driver-.md)|[Paradox](../content/SQLGetTypeInfo--Paradox-Driver-.md)|[Text File](../content/SQLGetTypeInfo--Text-File-Driver-.md)|[Excel](../content/SQLGetTypeInfo--Excel-Driver-.md)||  
|[SQLMoreResults](../content/SQLMoreResults-Function.md)||||||[All drivers](../content/SQLMoreResults--Desktop-Database-Drivers-.md)|  
|[SQLPrepare](../content/SQLPrepare-Function.md)||||||[All drivers](../content/SQLPrepare--Desktop-Database-Drivers-.md)|  
|[SQLProcedureColumns](../content/SQLProcedureColumns-Function.md)||||||[Access](../content/SQLProcedureColumns--Access-Driver-.md)|  
|[SQLProcedures](../content/SQLProcedures-Function.md)||||||[All drivers](../content/SQLProcedures--Desktop-Database-Drivers-.md)|  
|[SQLSetConnectOption](../content/SQLSetConnectOption-Function.md)|[Access](../content/SQLSetConnectOption--Access-Driver-.md)|[dBASE](../content/SQLSetConnectOption--dBASE-Driver-.md)|[Paradox](../content/SQLSetConnectOption--Paradox-Driver-.md)|[Text File](../content/SQLSetConnectOption--Text-File-Driver-.md)|[Excel](../content/SQLSetConnectOption--Excel-Driver-.md)||  
|[SQLSetCursorName](../content/SQLSetCursorName-Function.md)||||||[All drivers](../content/SQLSetCursorName--Desktop-Database-Drivers-.md)|  
|[SQLSetPos](../content/SQLSetPos-Function.md)||||||[All drivers](../content/SQLSetPos--Desktop-Database-Drivers-.md)|  
|[SQLSetScrollOptions](../content/SQLSetScrollOptions-Function.md)||||||[All drivers](../content/SQLSetScrollOptions--Desktop-Database-Drivers-.md)|  
|[SQLSetStmtOption](../content/SQLSetStmtOption-Function.md)||||||[All drivers](../content/SQLSetStmtOption--Desktop-Database-Drivers-.md)|  
|[SQLSpecialColumns](../content/SQLSpecialColumns-Function.md)||||||[All drivers](../content/SQLSpecialColumns--Desktop-Database-Drivers-.md)|  
|[SQLStatistics](../content/SQLStatistics-Function.md)|[Access](../content/SQLStatistics--Access-Driver-.md)|[dBASE](../content/SQLStatistics--dBASE-Driver-.md)|[Paradox](../content/SQLStatistics--Paradox-Driver-.md)|[Text File](../content/SQLStatistics--Text-File-Driver-.md)|[Excel](../content/SQLStatistics--Excel-Driver-.md)||  
|[SQLTables](../content/SQLTables-Function.md)|[Access](../content/SQLTables--Access-Driver-.md)|[dBASE](../content/SQLTables--dBASE-Driver-.md)|[Paradox](../content/SQLTables--Paradox-Driver-.md)|[Text File](../content/SQLTables--Text-File-Driver-.md)|[Excel](../content/SQLTables--Excel-Driver-.md)||  
Transact](../Topic/SQLTransact%20Function.md)|[Access](../content/SQLTransact--Access-Driver-.md)|[dBASE](../content/SQLTransact--dBASE-Driver-.md)|[Paradox](../content/SQLTransact--Paradox-Driver-.md)|[Text File](../content/SQLTransact--Text-File-Driver-.md)|[Excel](../content/SQLTransact--Excel-Driver-.md)||  
  
 The following topics provide remarks about ODBC functions. These remarks apply to all ODBC Desktop Database Drivers.  
  
-   [SQLGetData (Desktop Database Drivers)](../content/SQLGetData--Desktop-Database-Drivers-.md)  
  
-   [SQLGetStmtOption(Desktop Database Drivers)](../content/SQLGetStmtOption--Desktop-Database-Drivers-.md)  
  
-   [SQLMoreResults (Desktop Database Drivers)](../content/SQLMoreResults--Desktop-Database-Drivers-.md)  
  
-   [SQLPrepare (Desktop Database Drivers)](../content/SQLPrepare--Desktop-Database-Drivers-.md)  
  
-   [SQLProcedures (Desktop Database Drivers)](../content/SQLProcedures--Desktop-Database-Drivers-.md)  
  
-   [SQLSetCursorName (Desktop Database Drivers)](../content/SQLSetCursorName--Desktop-Database-Drivers-.md)  
  
-   [SQLSetPos (Desktop Database Drivers)](../content/SQLSetPos--Desktop-Database-Drivers-.md)  
  
-   [SQLSetScrollOptions (Desktop Database Drivers)](../content/SQLSetScrollOptions--Desktop-Database-Drivers-.md)  
  
-   [SQLSetStmtOption (Desktop Database Drivers)](../content/SQLSetStmtOption--Desktop-Database-Drivers-.md)  
  
-   [SQLSpecialColumns (Desktop Database Drivers)](../content/SQLSpecialColumns--Desktop-Database-Drivers-.md)