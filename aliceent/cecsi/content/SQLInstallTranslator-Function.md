---
title: "SQLInstallTranslator Function"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLInstallTranslator
apilocation: 
  - sqlsrv32.dll
apitype: dllExport
ms.assetid: 453b21ff-3c2b-4069-8ff7-5c727f062d89
caps.latest.revision: 7
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLInstallTranslator Function
**Conformance**  
 Version Introduced: ODBC 2.5, Deprecated  
  
 **Summary**  
 In ODBC 3.0, **SQLInstallTranslator** has been replaced by [SQLInstallTranslatorEx](../content/SQLInstallTranslatorEx-Function.md). Calls to **SQLInstallTranslator** will be mapped to **SQLInstallTranslatorEx**. For more information, see **SQLInstallTranslatorEx**.  
  
 **SQLInstallTranslator** will return FALSE if an application calls it in the ODBC 3*.x* Driver Manager with the *lpszInfFile* argument set to a value other than NULL. The Odbc.inf file used in ODBC 2.*x* is no longer supported in ODBC 3*.x*, even for backward compatibility.