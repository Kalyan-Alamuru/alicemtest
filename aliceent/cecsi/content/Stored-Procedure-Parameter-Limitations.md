---
title: "Stored Procedure Parameter Limitations"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8b804bcf-4cce-4e6f-aa45-00bab9ef9921
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Stored Procedure Parameter Limitations
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work, and plan to modify applications that currently use this feature. Instead, use the ODBC driver provided by Oracle.  
  
 When running Oracle stored procedures that utilize 10 or more output parameters, the stored procedure call will fail, resulting in an Access Violation or ActiveX Data Objects (ADO) error. This can occur when using the Microsoft ODBC Driver for Oracle with versions 8.0.4.0.0 and 8.0.4.0.4 of the Oracle client software.  
  
 To correct the problem, the Oracle client software must be upgraded to version 8.0.4.2.0 or higher. Contact Oracle Corporation for more information about the [patches](../content/Oracle-Software-Patches.md).  
  
> [!NOTE]  
>  This problem does not occur with the early release of Oracle client software version 8.0.3.0.0.