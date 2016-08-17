---
title: "SQLSetConnectOption (Text File Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b631a20c-2f60-4102-a61d-93b8780a4620
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLSetConnectOption (Text File Driver)
> [!NOTE]  
>  This topic provides Text File Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
|fOption|Comment|  
|-------------|-------------|  
|SQL_ACCESS_MODE|The SQL_ACCESS_MODE fOption can be set to either SQL_MODE_READ_ONLY or SQL_MODE_READ_WRITE. However, the driver does not prevent updates if SQL_ACCESS_MODE is set to SQL_MODE_READ_ONLY.|  
|SQL_AUTOCOMMIT|The Text driver only supports SQL_AUTOCOMMIT being set to ON (the default state), because they do not support transactions.|  
|SQL_CURRENT_QUALIFIER|Supported.|  
|SQL_LOGIN_TIMEOUT|Not supported.|  
|SQL_OPT_TRACE|Supported.|  
|SQL_OPT_TRACEFILE|Supported.|  
|SQL_PACKET_SIZE|Not supported.|  
|SQL_QUIET_MODE|Not supported.|  
|SQL_TRANSLATE_DLL|Not supported.|  
|SQL_TRANSLATION_OPTION|Not supported.|  
|SQL_TXN_ISOLATION|Not supported.|