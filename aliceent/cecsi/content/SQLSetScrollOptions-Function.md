---
title: "SQLSetScrollOptions Function"
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
  - SQLSetScrollOptions
apilocation: 
  - sqlsrv32.dll
apitype: dllExport
ms.assetid: 2a825ba7-7942-4c23-bcdb-c80dc12f8c86
caps.latest.revision: 12
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLSetScrollOptions Function
**Conformance**  
 Version Introduced: ODBC 1.0 Standards Compliance: Deprecated  
  
 **Summary**  
 In ODBC 3*.x*, the ODBC 2.0 function **SQLSetScrollOptions** has been replaced by calls to **SQLGetInfo** and **SQLSetStmtAttr**.  
  
> [!NOTE]  
>  For more information about what the Driver Manager maps this function to when an ODBC 2*.x* application is working with an ODBC 3*.x* driver, see [Mapping Deprecated Functions](../content/Mapping-Deprecated-Functions.md) in Appendix G: Driver Guidelines for Backward Compatibility.  
  
> [!NOTE]  
>  When the Driver Manager maps **SQLSetScrollOptions** for an application working with an ODBC 3*.x* driver that does not support **SQLSetScrollOptions**, the Driver Manager sets the SQL_ROWSET_SIZE statement option, not the SQL_ATTR_ROW_ARRAY_SIZE statement attribute, to the *RowsetSize* argument in **SQLSetScrollOption**. As a result, **SQLSetScrollOptions** cannot be used by an application when fetching multiple rows by a call to **SQLFetch** or **SQLFetchScroll**. It can be used only when fetching multiple rows by a call to **SQLExtendedFetch**.  
  
## Remarks  
 If your application will run on a 64-bit operating system, see [ODBC 64-Bit Information](../content/ODBC-64-Bit-Information.md).  
  
## See Also  
 [ODBC API Reference](../content/ODBC-API-Reference.md)   
 [ODBC Header Files](../content/ODBC-Header-Files.md)