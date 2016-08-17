---
title: "ODBC Drivers Subkey"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8edbf68f-d05d-4d77-92f6-e9500008f520
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# ODBC Drivers Subkey
The values under the ODBC Drivers subkey list the installed drivers. The format of these values is shown in the following table.  
  
|Name|Data type|Data|  
|----------|---------------|----------|  
|*driver-description*|REG_SZ|**Installed**|  
  
 The *driver-description* name is defined by the driver developer. It is usually the name of the DBMS associated with the driver.  
  
 For example, suppose drivers have been installed for formatted text files and SQL Server. The values under the ODBC Drivers subkey might be:  
  
```  
Text : REG_SZ : Installed  
SQL Server : REG_SZ : Installed  
```