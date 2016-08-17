---
title: "ODBC Core Subkey"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 055b31fc-f96c-450b-a596-d4570079fbf2
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# ODBC Core Subkey
The value under the ODBC Core subkey gives the usage count for the core components (Driver Manager, cursor library, installer DLL, and so on). The format of this value is shown in the following table.  
  
|Name|Data type|Data|  
|----------|---------------|----------|  
|UsageCount|REG_DWORD|*count*|  
  
 For example, suppose the ODBC Core components have been installed by the setup programs for three different applications and two different drivers. The value under the ODBC Core subkey would be:  
  
```  
UsageCount : REG_DWORD : 0x5  
```