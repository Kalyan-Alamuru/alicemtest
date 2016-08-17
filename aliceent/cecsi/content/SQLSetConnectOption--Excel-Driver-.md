---
title: "SQLSetConnectOption (Excel Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 528d21d1-4516-4497-9da4-7b87d77e622a
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLSetConnectOption (Excel Driver)
> [!NOTE]  
>  This topic provides Excel Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
|fOption|Comment|  
|-------------|-------------|  
|SQL_ACCESS_MODE|The SQL_ACCESS_MODE fOption can be set to either SQL_MODE_READ_ONLY or SQL_MODE_READ_WRITE. However, the driver does not prevent updates if SQL_ACCESS_MODE is set to SQL_MODE_READ_ONLY.|  
|SQL_AUTOCOMMIT|The Microsoft Excel driver only supports SQL_AUTOCOMMIT being set to ON (the default state), because they do not support transactions.|  
|SQL_CURRENT_QUALIFIER|Supported.|  
|SQL_LOGIN_TIMEOUT|Not supported.|  
|SQL_OPT_TRACE|Supported.|  
|SQL_OPT_TRACEFILE|Supported.|  
|SQL_PACKET_SIZE|Not supported.|  
|SQL_QUIET_MODE|Not supported.|  
|SQL_TRANSLATE_DLL|Not supported.|  
|SQL_TRANSLATION_OPTION|Not supported.|  
|SQL_TXN_ISOLATION|Not supported.|