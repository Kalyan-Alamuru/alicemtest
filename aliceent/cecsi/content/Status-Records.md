---
title: "Status Records"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4a987f69-158f-4cc4-a31b-2b7dd8dcbb87
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Status Records
The fields in the status records contain information about specific errors or warnings returned by the Driver Manager, driver, or data source, including the SQLSTATE, native error number, diagnostic message, column number, and row number. Status records can be created only if the function returns SQL_ERROR, SQL_SUCCESS_WITH_INFO, SQL_NO_DATA, SQL_NEED_DATA, or SQL_STILL_EXECUTING. For a complete list of fields in the status records, see the [SQLGetDiagField](../content/SQLGetDiagField-Function.md) function description.  
  
 This section contains the following topics.  
  
-   [Sequence of Status Records](../content/Sequence-of-Status-Records.md)  
  
-   [SQLSTATEs](../content/SQLSTATEs.md)  
  
-   [Diagnostic Messages](../content/Diagnostic-Messages.md)