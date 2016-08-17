---
title: "SQLGetConfigMode Function"
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
  - SQLGetConfigMode
apilocation: 
  - sqlsrv32.dll
apitype: dllExport
ms.assetid: b96ab3b8-08d5-4fea-9ffe-e03043efbf2d
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLGetConfigMode Function
**Conformance**  
 Version Introduced: ODBC 3.0  
  
 **Summary**  
 **SQLGetConfigMode** retrieves the configuration mode that indicates where the Odbc.ini entry listing DSN values is in the system information.  
  
## Syntax  
  
```  
  
BOOL SQLGetConfigMode(  
     UWORD *   pwConfigMode);  
```  
  
## Arguments  
 *pwConfigMode*  
 [Output] Pointer to the buffer containing the configuration mode. (See "Comments.") The value in *\*pwConfigMode* can be:  
  
 ODBC_USER_DSN  
  
 ODBC_SYSTEM_DSN  
  
 ODBC_BOTH_DSN  
  
## Returns  
 The function returns TRUE if it is successful, FALSE if it fails.  
  
## Diagnostics  
 When **SQLGetConfigMode** returns FALSE, an associated *\*pfErrorCode* value can be obtained by calling **SQLInstallerError**. The following table lists the *\*pfErrorCode* values that can be returned by **SQLInstallerError** and explains each one in the context of this function.  
  
|*\*pfErrorCode*|Error|Description|  
|---------------------|-----------|-----------------|  
|ODBC_ERROR_OUT_OF_MEM|Out of memory|The installer could not perform the function because of a lack of memory.|  
  
## Comments  
 This function is used to determine where the Odbc.ini entry listing DSN values is in the system information. If *\*pwConfigMode* is ODBC_USER_DSN, the DSN is a User DSN and the function reads from the Odbc.ini entry in HKEY_CURRENT_USER. If it is ODBC_SYSTEM_DSN, the DSN is a System DSN and the function reads from the Odbc.ini entry in HKEY_LOCAL_MACHINE. If it is ODBC_BOTH_DSN, HKEY_CURRENT_USER is tried, and if it fails, HKEY_LOCAL_MACHINE is used.  
  
 By default, **SQLGetConfigMode** returns ODBC_BOTH_DSN. When a User DSN or a System DSN is created by a call to **SQLConfigDataSource**, the function sets the configuration mode to ODBC_USER_DSN or ODBC_SYSTEM_DSN to distinguish user and System DSNs while modifying a DSN. Prior to returning, **SQLConfigDataSource** resets the configuration mode to ODBC_BOTH_DSN.  
  
## Related Functions  
  
|For information about|See|  
|---------------------------|---------|  
|Setting the configuration mode|[SQLSetConfigMode](../content/SQLSetConfigMode-Function.md)|