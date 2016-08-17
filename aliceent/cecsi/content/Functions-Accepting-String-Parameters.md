---
title: "Functions Accepting String Parameters"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 869b8421-f71e-4dfd-adce-691bd3012b16
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Functions Accepting String Parameters
All functions that take string parameters will be converted to Unicode. (The "W" form of the function will be exported.) Count of bytes is converted to count of characters for those applicable ODBC APIs. This applies to the following functions:  
  
-   **SQLConnect**  
  
-   **SQLDriverConnect**  
  
-   **SQLColAttributes**  
  
-   **SQLDescribeCol**  
  
-   **SQLError** (replaced by **SQLGetDiagField**)  
  
-   **SQLExecDirect**  
  
-   **SQLGetCursorName**  
  
-   **SQLSetCursorName**  
  
-   **SQLGetStmtAttr**  
  
-   **SQLGetInfo**  
  
-   **SQLGetStmtOption** (becomes **SQLGetStmtAttr**)  
  
-   **SQLSetStmtOption** (becomes **SQLSetStmtAttr**)  
  
-   **SQLGetConnectOption**  
  
-   **SQLSetConnectOption**  
  
-   **SQLGetTypeInfo**  
  
-   **SQLStatistics**  
  
-   **SQLTables**  
  
-   **SQLNativeSQL**  
  
-   **SQLSpecialColumns**  
  
-   **ConfigDSNEx**  
  
-   **ConfigDSN**