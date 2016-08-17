---
title: "Procedure Invocation"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b9ff2c3a-2003-4832-adbe-08dd0f5ad948
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Procedure Invocation
When the Microsoft Access driver is used, procedures can be invoked from the driver by using the **SQLExecDirect** or **SQLPrepare** function with the following syntax: {CALL *procedure-name* [(*parameter*[,*parameter*]...)]}. Note that expressions are not supported as parameters to a called procedure.  
  
 If a procedure name includes a dash, the name must be delimited with back quotes (`).  
  
 A parameterized query can be called using the previous statement.