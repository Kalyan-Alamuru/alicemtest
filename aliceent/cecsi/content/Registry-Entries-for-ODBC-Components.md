---
title: "Registry Entries for ODBC Components"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c90aa8a4-6ece-48de-901c-17d23739a9ff
caps.latest.revision: 9
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Registry Entries for ODBC Components
> [!NOTE]  
>  Starting with Windows XP and Windows Server 2003, ODBC is included in the Windows operation system. You should only explicitly install ODBC on earlier versions of Windows.  
  
 The installer DLL maintains information in the registry about each installed ODBC component. On computers running Microsoft Windows NT and Microsoft Windows 95/98, this information is stored in subkeys under the following key in the registry:  
  
 HKEY_LOCAL_MACHINE  
  
 SOFTWARE  
  
 ODBC  
  
 Odbcinst.ini  
  
 Because Odbcinst.ini is a subkey of the HKEY_LOCAL_MACHINE tree, the information about ODBC components is available to all users of the machine.  
  
 This section contains the following topics.  
  
-   [ODBC Core Subkey](../content/ODBC-Core-Subkey.md)  
  
-   [ODBC Drivers Subkey](../content/ODBC-Drivers-Subkey.md)  
  
-   [Driver Specification Subkeys](../content/Driver-Specification-Subkeys.md)  
  
-   [Default Driver Subkey](../content/Default-Driver-Subkey.md)  
  
-   [ODBC Translators Subkey](../content/ODBC-Translators-Subkey.md)  
  
-   [Translator Specification Subkeys](../content/Translator-Specification-Subkeys.md)