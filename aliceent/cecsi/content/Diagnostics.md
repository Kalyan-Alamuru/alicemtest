---
title: "Diagnostics"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 450abd88-90a1-4fbc-b417-8efbdd8e1dea
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Diagnostics
Functions in ODBC return diagnostic information in two ways. The return code indicates the overall success or failure of the function, while diagnostic records provide detailed information about the function. At least one diagnostic record — the header record — is returned even if the function succeeds.  
  
 Diagnostic information is used at development time to catch programming errors such as invalid handles and syntax errors in hard-coded SQL statements. It is used at run time to catch run-time errors and warnings such as data truncation, access violations, and syntax errors in SQL statements entered by the user.  
  
 This section contains the following topics.  
  
-   [Return Codes](../content/Return-Codes-ODBC.md)  
  
-   [Diagnostic Records](../content/Diagnostic-Records.md)  
  
-   [Using SQLGetDiagRec and SQLGetDiagField](../content/Using-SQLGetDiagRec-and-SQLGetDiagField.md)  
  
-   [Implementing SQLGetDiagRec and SQLGetDiagField](../content/Implementing-SQLGetDiagRec-and-SQLGetDiagField.md)  
  
-   [Diagnostic Handling Examples](../content/Diagnostic-Handling-Examples.md)