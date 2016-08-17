---
title: "Revoking and Granting Rights When Using Stored Procedures"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 24070039-03ab-4623-a681-6308802eb399
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Revoking and Granting Rights When Using Stored Procedures
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work, and plan to modify applications that currently use this feature. Instead, use the ODBC driver provided by Oracle.  
  
 The Microsoft ODBC Driver for Oracle returns the following error message when user rights are granted and then revoked on a table accessed by a stored procedure:  
  
 SQL_ERROR=-1  
  
 szErrorMsg="[Microsoft][ODBC driver for Oracle]Wrong number of parameters"  
  
 szErrorMsg="[Microsoft][ODBC driver for Oracle]Syntax error or access violation"  
  
 The call to the Oracle OCI function Odessp() fails in this scenario but is necessary in order to implement default parameters. After the underlying table permissions are modified, the stored procedure must be recompiled before running it again.