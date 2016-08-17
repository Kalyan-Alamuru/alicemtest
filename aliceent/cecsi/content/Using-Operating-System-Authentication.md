---
title: "Using Operating System Authentication"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 613daef7-3171-42d0-b7e3-3879280f864d
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Using Operating System Authentication
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work, and plan to modify applications that currently use this feature. Instead, use the ODBC driver provided by Oracle.  
  
 Oracle operating system authentication relies on the underlying operating system to control access to database accounts. Users need not enter a password when using this type of login.  
  
 To take advantage of this feature, specify "/" as the user ID and do not specify a password when connecting using any of the following connection APIs: [SQLBrowseConnect](../content/Level-2-API-Functions--ODBC-Driver-for-Oracle-.md), [SQLConnect](../content/Core-Level-API-Functions--ODBC-Driver-for-Oracle-.md), or [SQLDriverConnect](../content/Level-1-API-Functions--ODBC-Driver-for-Oracle-.md).  
  
 Oracle databases use SQL*Net Authentication Services to authenticate users that are logged on. This service works well if users are logged into Oracle through SQLPlus; however, when the logged-in user is a service such as Internet Information Services, the authentication fails. This is a known limitation of SQL\*Net Authentication and produces the following error: "[Microsoft][ODBC driver for Oracle][Oracle]ORA-12641: TNS:authentication service failed to initialize."  
  
 You can correct this problem by editing the Sqlnet.ora file. This configuration file is usually stored in the Network\Admin subdirectory of the Oracle home directory. Add the following line to Sqlnet.ora:  
  
```  
SQLNET.AUTHENTICATION_SERVICES = (none)  
```