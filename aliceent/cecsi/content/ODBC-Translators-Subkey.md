---
title: "ODBC Translators Subkey"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6b170f1f-e263-4aac-9d49-8d0ca0470ca2
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# ODBC Translators Subkey
The values under the ODBC Translators subkey list the installed translators. The format of these values is shown in the following table.  
  
|Name|Data type|Data|  
|----------|---------------|----------|  
|*translator-desc*|REG_SZ|**Installed**|  
  
 The *translator-desc* name is defined by the translator developer.  
  
 For example, suppose a user has installed the Microsoft® Code Page Translator and a custom ASCII to EBCDIC translator. The values under the ODBC Translators subkey might be as follows:  
  
```  
MS Code Page Translator: REG_SZ : Installed  
ASCII to EBCDIC: REG_SZ : Installed.  
```