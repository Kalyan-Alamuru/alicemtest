---
title: "Translator Setup DLLs"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b3ca79e9-01b9-4541-81de-bbbad24ca736
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Translator Setup DLLs
> [!NOTE]  
>  Starting with Windows XP and Windows Server 2003, ODBC is included in the Windows operation system. You should only explicitly install ODBC on earlier versions of Windows.  
  
 The translator setup DLL contains the **ConfigTranslator** function, which returns the default option for a translator. If necessary, it prompts the user for this information. For a complete description of this function, see [Setup DLL API Reference](../content/Setup-DLL-API-Reference.md).  
  
 The translator setup DLL is written by the translator developer. It can be part of the translator DLL or a separate DLL.