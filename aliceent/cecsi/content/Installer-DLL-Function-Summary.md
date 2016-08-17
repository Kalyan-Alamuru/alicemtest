---
title: "Installer DLL Function Summary"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 666c09d3-1e10-4d89-9b42-eda2957a87f0
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Installer DLL Function Summary
The following table describes the functions in the installer DLL. For more information about the syntax and semantics for each function, see [Installer DLL API Reference](../content/Installer-DLL-API-Reference-Function.md).  
  
|Task|Function name|Purpose|  
|----------|-------------------|-------------|  
|Installing ODBC|[SQLConfigDriver](../content/SQLConfigDriver-Function.md)|Loads the driver-specific setup DLL.|  
||[SQLGetInstalledDrivers](../content/SQLGetInstalledDrivers-Function.md)|Returns a list of installed drivers.|  
||[SQLInstallDriverEx](../content/SQLInstallDriverEx-Function.md)|Adds a driver to the system information.|  
||[SQLInstallDriverManager](../content/SQLInstallDriverManager-Function.md)|Returns the target directory for the Driver Manager.|  
||[SQLInstallerError](../content/SQLInstallerError-Function.md)|Returns error or status information for the installer functions.|  
||[SQLInstallTranslatorEx](../content/SQLInstallTranslatorEx-Function.md)|Adds a translator to the system information.|  
||[SQLPostInstallerError](../content/SQLPostInstallerError-Function.md)|Allows a driver or translator setup library to report errors.|  
||[SQLRemoveDriver](../content/SQLRemoveDriver-Function.md)|Removes a driver from the system information.|  
||[SQLRemoveDriverManager](../content/SQLRemoveDriverManager-Function.md)|Removes ODBC core components from the system information.|  
||[SQLRemoveTranslator](../content/SQLRemoveTranslator-Function.md)|Removes the translator from the system information.|  
|Configuring data sources|[SQLConfigDataSource](../content/SQLConfigDataSource-Function.md)|Calls the driver-specific setup DLL.|  
||[SQLCreateDataSource](../content/SQLCreateDataSource-Function.md)|Displays a dialog box to add a data source.|  
||[SQLGetConfigMode](../content/SQLGetConfigMode-Function.md)|Retrieves the configuration mode that indicates where the Odbc.ini entry listing DSN values is in the system information.|  
||[SQLGetPrivateProfileString](../content/SQLGetPrivateProfileString-Function.md)|Writes a value to the system information.|  
||[SQLGetTranslator](../content/SQLGetTranslator-Function.md)|Displays a dialog box to select a translator.|  
||[SQLManageDataSources](../content/SQLManageDataSources.md)|Displays a dialog box to configure data sources and drivers.|  
||[SQLReadFileDSN](../content/SQLReadFileDSN-Function.md)|Reads information from file DSNs.|  
||[SQLRemoveDefaultDataSource](../content/SQLRemoveDefaultDataSource-Function.md)|Removes the default data source.|  
||[SQLRemoveDSNFromIni](../content/SQLRemoveDSNFromIni-Function.md)|Removes a data source.|  
||[SQLSetConfigMode](../content/SQLSetConfigMode-Function.md)|Sets the configuration mode that indicates where the Odbc.ini entry listing DSN values is in the system information.|  
||[SQLValidDSN](../content/SQLValidDSN-Function.md)|Checks the length and validity of the data source name.|  
||[SQLWriteDSNToIni](../content/SQLWriteDSNToIni-Function.md)|Adds a data source.|  
||[SQLWriteFileDSN](../content/SQLWriteFileDSN-Function.md)|Writes information to file DSNs.|  
||[SQLWritePrivateProfileString](../content/SQLWritePrivateProfileString-Function.md)|Gets a value from the system information.|