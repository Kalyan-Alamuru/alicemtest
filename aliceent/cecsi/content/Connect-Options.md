---
title: "Connect Options"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: abfdc133-cb33-435f-a467-fbe15444f687
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Connect Options
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work, and plan to modify applications that currently use this feature. Instead, use the ODBC driver provided by Oracle.  
  
 These options allow customization of the database connection within an application.  
  
|Connect option|Notes|  
|--------------------|-----------|  
|SQL_AUTOCOMMIT|If you choose SQL_AUTOCOMMIT_OFF, your application must explicitly commit or roll back transactions with [SQLTransact](../content/Core-Level-API-Functions--ODBC-Driver-for-Oracle-.md).|  
|SQL_ODBC_CURSORS|This connection attribute is implemented in the Driver Manager.|  
|SQL_OPT_TRACE|This connection attribute is implemented in the Driver Manager.|  
|SQL_OPT_TRACEFILE|This connection attribute is implemented in the Driver Manager.|  
|SQL_TRANSLATE_DLL|Returns error: "Driver not capable."|  
|SQL_TRANSLATE_OPTION|A 32-bit value passed to the translation .dll.|  
|SQL_TXN_ISOLATION|The driver allows only SQL_TXN_READ_COMMITTED.<br /><br /> The following vParams are not supported:<br /><br /> SQL_TXN_READ_UNCOMMITTED<br /><br /> SQL_TXN_REAPEATABLE_READ<br /><br /> SQL_TXN_SERIALIZABLE|  
|SQL_ATTR_ENLIST_IN_DTC|This ODBC 3.0 connection attribute allows you to use the ODBC Driver for Oracle in distributed transactions coordinated by Microsoft Component Services (or MTS, if you are using Windows NT). It provides the interface pointer *pITransaction* to the transaction as the *vParam* argument.|  
|SQL_ATTR_CONNECTION_DEAD|This read-only ODBC 3.5 connection attribute allows you to determine whether the connection to the Oracle server has failed. Get only; cannot Set.|