---
title: "SQLPostInstallerError Function"
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
  - SQLPostInstallerError
apilocation: 
  - sqlsrv32.dll
apitype: dllExport
ms.assetid: 4c60d827-b2d2-4f27-b220-daa9e1fcdd8d
caps.latest.revision: 7
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLPostInstallerError Function
**Conformance**  
 Version Introduced: ODBC 3.0  
  
 **Summary**  
 **SQLPostInstallerError** provides a mechanism for a driver or translator setup library to report errors for the **ConfigDriver**, **ConfigDSN**, and **ConfigTranslator** functions to the installer error queue. Applications do not use this API; they use **SQLInstallerError** to retrieve the error.  
  
## Syntax  
  
```  
  
RETCODE SQLPostInstallerError(  
     DWORD    fErrorCode,  
     LPSTR    szErrorMsg);  
```  
  
## Arguments  
 *fErrorCode*  
 [Input] Installer error code.  
  
 *szErrorMsg*  
 [Input] Error message text.  
  
## Returns  
 SQL_SUCCESS or SQL_ERROR.  
  
## Diagnostics  
 **SQLPostInstallerError** does not post error values for itself. If the error was successfully posted to the installer error queue (retrievable using **SQLInstallerError**), SQL_SUCCESS is returned. SQL_ERROR will be returned if the value in the *dwErrorCode* argument is not one of the specified installer error codes.  
  
## Related Functions  
  
|For information about|See|  
|---------------------------|---------|  
|Adding, modifying, or removing a driver|[ConfigDriver](../content/ConfigDriver-Function.md)|  
|Adding, modifying, or removing data sources|[ConfigDSN](../content/ConfigDSN-Function.md)|  
|Setting a translation option|[ConfigTranslator](../content/ConfigTranslator-Function.md)|