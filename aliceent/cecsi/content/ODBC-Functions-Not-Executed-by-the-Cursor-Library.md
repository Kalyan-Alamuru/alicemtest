---
title: "ODBC Functions Not Executed by the Cursor Library"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f2941522-75eb-4db9-9468-4800b884dac2
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# ODBC Functions Not Executed by the Cursor Library
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work and plan to modify applications that currently use this feature. Microsoft recommends using the driver's cursor functionality.  
  
 The cursor library does not execute the following functions. When an application calls one of these functions, the Driver Manager invokes the driver, not the cursor library.  
  
|||  
|-|-|  
|**SQLFetch**|**SQLGetEnvAttr**|  
|**SQLGetConnectAttr**|**SQLSetDescRec**|  
|**SQLGetDiagField**|**SQLSetEnvAttr**|  
|**SQLGetDiagRec**||