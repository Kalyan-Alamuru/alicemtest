---
title: "Configuration Components"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0b68ff48-12e4-41aa-b9e2-b39ed5023ea7
caps.latest.revision: 11
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Configuration Components
> [!NOTE]  
>  Starting with Windows XP and Windows Server 2003, ODBC is included in the Windows operation system. You should only explicitly install ODBC on earlier versions of Windows.  
  
 Data sources are configured by the installer DLL, which in turn calls driver setup DLLs and translator setup DLLs as they are needed. The installer DLL is either invoked directly from Control Panel or loaded and called by another program, known as the *administration program*. The following illustration shows the relationship between the configuration components.  
  
 ![Relationship between configuration components](../content/media/pr30.gif "pr30")  
  
 For more information about these components, see the following topics at the end of this section.  
  
-   [Setup Program](../content/Setup-Program.md)  
  
-   [Installer DLL](../content/Installer-DLL.md)  
  
-   [Driver Setup DLL](../content/Driver-Setup-DLL.md)  
  
## See Also  
 [Installation Components](../content/Installation-Components.md)