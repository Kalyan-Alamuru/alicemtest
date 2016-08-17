---
title: "SQLSetConnectOption Function"
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
  - SQLSetConnectOption
apilocation: 
  - sqlsrv32.dll
apitype: dllExport
ms.assetid: 8cd2c2a2-25c8-4aff-951c-b593bbfc90ad
caps.latest.revision: 12
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLSetConnectOption Function
**Conformance**  
 Version Introduced: ODBC 1.0 Standards Compliance: Deprecated  
  
 **Summary**  
 In ODBC 3*.x*, the ODBC 2.0 function **SQLSetConnectOption** has been replaced by **SQLSetConnectAttr**. For more information, see [SQLSetConnectAttr](../content/SQLSetConnectAttr-Function.md).  
  
> [!NOTE]  
>  For more information about what the Driver Manager maps this function to when an ODBC 2*.x* application is working with an ODBC 3*.x* driver, see [Mapping Deprecated Functions](../content/Mapping-Deprecated-Functions.md)".  
  
## Remarks  
 See [ODBC 64-Bit Information](../content/ODBC-64-Bit-Information.md), if your application will run on a 64-bit operating system.  
  
> [!NOTE]  
>  The attribute SQL_ASYNC_DBC_FUNCTION_ENABLE introduced in ODBC 3.8 is not supported by **SQLSetConnectOption**. Applications that use the asynchronous operation on connection handle must use **SQLSetConnectAttr**.  
  
## See Also  
 [ODBC API Reference](../content/ODBC-API-Reference.md)   
 [ODBC Header Files](../content/ODBC-Header-Files.md)