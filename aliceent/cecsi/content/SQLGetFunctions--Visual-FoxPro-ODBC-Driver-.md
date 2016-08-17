---
title: "SQLGetFunctions (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8102932a-88b3-49d8-bf7a-c766f54878c0
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLGetFunctions (Visual FoxPro ODBC Driver)
> [!NOTE]  
>  This topic contains Visual FoxPro ODBC Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Support: Full  
  
 ODBC API Conformance: Level 1  
  
 Returns TRUE for all supported functions.  
  
 The Visual FoxPro ODBC Driver supports all ODBC API Core and Level 1 functions. The following table indicates whether the driver supports a specific Level 2 function.  
  
|*Function*|Supported|  
|----------------|---------------|  
|SQL_API_SQLBROWSECONNECT|No|  
|SQL_API_SQLCOLUMNPRIVELEGES|No|  
|SQL_API_SQLDATASOURCES|Yes|  
|SQL_API_SQLDESCRIBEPARAM|No|  
|SQL_API_SQLDRIVERS|Yes|  
|SQL_API_SQLEXTENDEDFETCH|Yes|  
|SQL_API_SQLFOREIGNKEYS|No|  
|SQL_API_SQLMORERESULTS|Yes|  
|SQL_API_SQLNATIVESQL|No|  
|SQL_API_SQLNUMPARAMS|Yes|  
|SQL_API_SQLPARAMOPTIONS|Yes|  
|SQL_API_SQLPRIMARYKEYS|Yes|  
|SQL_API_SQLPROCEDURECOLUMNS|No|  
|SQL_API_SQLPROCEDURES|No|  
|SQL_API_SQLSETPOS|Yes|  
|SQL_API_SQLSETSCROLLOPTIONS|Yes|  
|SQL_API_SQLTABLEPRIVILEGES|No|  
  
 For more information, see [SQLGetFunctions](../content/SQLGetFunctions-Function.md) in the *ODBC Programmer's Reference*.