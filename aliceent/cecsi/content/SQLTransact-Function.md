---
title: "SQLTransact Function"
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
  - SQLTransact
apilocation: 
  - sqlsrv32.dll
apitype: dllExport
ms.assetid: 496249e0-8eff-4c60-8358-5543bc3ead9c
caps.latest.revision: 13
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLTransact Function
**Conformance**  
 Version Introduced: ODBC 1.0 Standards Compliance: Deprecated  
  
 **Summary**  
 In ODBC 3.*x*, the ODBC 2*.x* function **SQLTransact** has been replaced by **SQLEndTran**. For more information, see [SQLEndTran](../content/SQLEndTran-Function.md).  
  
> [!NOTE]  
>  The attribute SQL_ASYNC_DBC_FUNCTION_ENABLE, which was introduced in ODBC 3.8, is not supported by **SQLTransact**. Applications using an asynchronous operation on a connection handle must use **SQLEndTran**.  
  
## See Also  
 [ODBC API Reference](../content/ODBC-API-Reference.md)   
 [ODBC Header Files](../content/ODBC-Header-Files.md)