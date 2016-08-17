---
title: "SQLGetConnectOption Function"
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
  - SQLGetConnectOption
apilocation: 
  - sqlsrv32.dll
apitype: dllExport
ms.assetid: 59cde899-7957-4b5e-8677-f34d3b859bfd
caps.latest.revision: 11
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLGetConnectOption Function
**Conformance**  
 Version Introduced: ODBC 1.0 Standards Compliance: Deprecated  
  
 **Summary**  
 In ODBC 3*.x*, the ODBC 2*.x* function **SQLGetConnectOption** has been replaced by **SQLGetConnectAttr**. For more information, see [SQLGetConnectAttr](../content/SQLGetConnectAttr-Function.md).  
  
> [!NOTE]  
>  For more information about what the Driver Manager maps this function to when an ODBC 2*.x* application is working with an ODBC 3*.x* driver, see [Mapping Deprecated Functions](../content/Mapping-Deprecated-Functions.md) in Appendix G: Driver Guidelines for Backward Compatibility.  
  
> [!NOTE]  
>  The attribute SQL_ASYNC_DBC_FUNCTION_ENABLE introduced in ODBC 3.8 is not supported by **SQLGetConnectOption**. Applications that use the asynchronous operation on a connection handle must use **SQLGetConnectAttr**.  
  
## See Also  
 [ODBC API Reference](../content/ODBC-API-Reference.md)   
 [ODBC Header Files](../content/ODBC-Header-Files.md)