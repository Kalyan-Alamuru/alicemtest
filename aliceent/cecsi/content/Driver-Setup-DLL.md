---
title: "Driver Setup DLL"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 49bab021-81fa-402e-b7a4-a5214f1fadc4
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Driver Setup DLL
> [!NOTE]  
>  Starting with Windows XP and Windows Server 2003, ODBC is included in the Windows operation system. You should only explicitly install ODBC on earlier versions of Windows.  
  
 The driver setup DLL contains the **ConfigDriver** and **ConfigDSN** functions. **ConfigDriver** performs driver-specific installation tasks, such as entering driver-specific information into the registry. **ConfigDSN** maintains driver-specific information about data sources in the registry. For a complete description of these functions, see [Setup DLL API Reference](../content/Setup-DLL-API-Reference.md).  
  
 **ConfigDSN** calls the following functions in the installer DLL to maintain data source information in the registry:  
  
-   **SQLWriteDSNToIni**. Add a data source.  
  
-   **SQLRemoveDSNFromIni**. Delete a data source.  
  
-   **SQLWritePrivateProfileString**. Write a driver-specific value under a data source specification subkey.  
  
-   **SQLGetPrivateProfileString**. Read a driver-specific value from a data source specification subkey.  
  
-   **SQLGetTranslator**. Prompt the user for a translator name and option. This function calls **ConfigTranslator** in the translator setup DLL.  
  
 The driver setup DLL is written by the driver developer. It can be part of the driver DLL or a separate DLL.