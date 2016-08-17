---
title: "Installation Components"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9de15ca0-fe6a-4634-8709-a928d3c9cc73
caps.latest.revision: 10
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Installation Components
> [!NOTE]  
>  Starting with Windows XP and Windows Server 2003, ODBC is included in the Windows operation system. You should only explicitly install ODBC on earlier versions of Windows.  
  
 The installation process starts when the user runs the setup program. The setup program works in conjunction with the *installer DLL* and a *driver setup DLL* for each driver. Both the setup program and the installer DLL use the arguments in the **SQLInstallDriverEx** and **SQLInstallTranslatorEx** functions to determine which files to copy or delete for each component. The following illustration shows the relationship between these installation components.  
  
 ![Relationship between installation components](../content/media/pr29.gif "pr29")  
  
> [!IMPORTANT]  
>  The Odbc.inf file that was used in ODBC 2.*x* to describe the files required by each ODBC component is not used in ODBC 3*.x*. Drivers that ship ODBC 3*.x* components do not need to create an Odbc.inf file. The removal of **SQLInstallDriver** and **SQLInstallODBC**, and the deprecation of **SQLInstallTranslator**, have rendered Odbc.inf unnecessary. The driver information that used to be in the Driver Keyword sections of Odbc.inf is now provided in the *lpszDriver* argument in **SQLInstallDriverEx**. The translator information that used to be in the [ODBC Translator] and Translator Specification sections of Odbc.inf is now provided in the *lpszTranslator* argument of **SQLInstallTranslatorEx**. These changes allow the ODBC Installer to be more portable across platforms.  
  
 For more information about these components, see the following topics at the end of this section.  
  
-   [Setup Program](../content/Setup-Program.md)  
  
-   [Installer DLL](../content/Installer-DLL.md)  
  
-   [Driver Setup DLL](../content/Driver-Setup-DLL.md)