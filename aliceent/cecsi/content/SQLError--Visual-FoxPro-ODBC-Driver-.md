---
title: "SQLError (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8315ec16-1c22-447a-a577-39bd94f61070
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLError (Visual FoxPro ODBC Driver)
> [!NOTE]  
>  This topic contains Visual FoxPro ODBC Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 Support: Full  
  
 ODBC API Conformance: Core Level  
  
 Returns error or status information about the last error. The driver maintains a stack or list of errors that can be returned for the *hstmt*, *hdbc*, and *henv* arguments, depending on how the call to **SQLError** is made. The error queue is flushed after each statement.  
  
 The following table describes the **SQLError** arguments and return values used by the driver.  
  
|SQLError argument|Return value description|  
|-----------------------|------------------------------|  
|*szSQLState*|The value for the SQLSTATE represented by the error.|  
|*pfNativeError*|A nonzero value indicates a [Visual FoxPro ODBC Driver Native Error Message](../content/Visual-FoxPro-ODBC-Driver-Native-Error-Messages.md). A value of zero indicates the error has been detected by the driver and mapped to the appropriate [ODBC Error Code](../content/ODBC-Error-Codes--Visual-FoxPro-ODBC-Driver-.md).|  
|*szErrorMsg*|The text for the native error or ODBC error.|  
|*pcbErrorMsg*|The length of the message text plus the length of the identifiers.|  
  
 For more information on driver error messages, see [Error Messages Overview](../content/Error-Messages--Visual-FoxPro-ODBC-Driver-.md). For more information about this function, see [SQLError](../content/SQLError-Function.md) in the *ODBC Programmer's Reference*.