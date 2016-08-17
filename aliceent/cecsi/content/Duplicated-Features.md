---
title: "Duplicated Features"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 641b16bc-f791-46d8-b093-31736473fe3d
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Duplicated Features
The following ODBC 2.*x* functions have been duplicated by ODBC 3.*x* functions. As a result, the ODBC 2.*x* functions are deprecated in ODBC 3.*x*. The ODBC 3.*x* functions are referred to as replacement functions.  
  
 When an application uses a deprecated ODBC 2.*x* function and the underlying driver is an ODBC 3.*x* driver, the Driver Manager maps the function call to the corresponding replacement function. The only exception to this rule is **SQLExtendedFetch**. (See the footnote at the end of the following table.) For more information about these mappings, see [Mapping Deprecated Functions](../content/Mapping-Deprecated-Functions.md) in Appendix G: Driver Guidelines for Backward Compatibility.  
  
 When an application uses a replacement function and the underlying driver is an ODBC 2.*x* driver, the Driver Manager maps the function call to the corresponding deprecated function.  
  
|ODBC 2.*x* function|ODBC 3.*x* function|  
|-------------------------|-------------------------|  
|**SQLAllocConnect**|**SQLAllocHandle**|  
|**SQLAllocEnv**|**SQLAllocHandle**|  
|**SQLAllocStmt**|**SQLAllocHandle**|  
|**SQLColAttributes**|**SQLColAttribute**|  
|**SQLError**|**SQLGetDiagRec**|  
|**SQLExtendedFetch**[1]|**SQLFetchScroll**|  
|**SQLFreeConnect**|**SQLFreeHandle**|  
|**SQLFreeEnv**|**SQLFreeHandle**|  
|**SQLGetConnectOption**|**SQLGetConnectAttr**|  
|**SQLGetStmtOption**|**SQLGetStmtAttr**|  
|**SQLParamOptions**|**SQLSetStmtAttr**, **SQLGetStmtAttr**|  
|**SQLSetConnectOption**|**SQLSetConnectAttr**|  
|**SQLSetParam**|**SQLBindParameter**|  
|**SQLSetStmtOption**|**SQLSetStmtAttr**|  
|**SQLTransact**|**SQLEndTran**|  
  
 [1]   The function **SQLExtendedFetch** is duplicated functionality; **SQLFetchScroll** provides the same functionality in ODBC 3.*x*. However, the Driver Manager does not map **SQLExtendedFetch** to **SQLFetchScroll** when going against an ODBC 3.*x* driver. For more information, see [What the Driver Manager Does](../content/What-the-Driver-Manager-Does.md) in Appendix G: Driver Guidelines for Backward Compatibility. The Driver Manager maps **SQLFetchScroll** to **SQLExtendedFetch** when going against an ODBC 2.*x* driver.  
  
> [!NOTE]  
>  The function **SQLBindParam** is a special case. **SQLBindParam** is duplicated functionality. This is not an ODBC 2*.x* function, but a function that is present in the Open Group and ISO standards. The functionality provided by this function is completely subsumed by that of **SQLBindParameter**. As a result, the Driver Manager maps a call to **SQLBindParam** to **SQLBindParameter** when the underlying driver is an ODBC 3.*x* driver. However, when the underlying driver is an ODBC 2*.x* driver, the Driver Manager does not perform this mapping.