---
title: "Cursor Library Operations"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 04d514b1-dc4d-4b84-bf35-60f4657ef1f6
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Cursor Library Operations
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work and plan to modify applications that currently use this feature. Microsoft recommends using the driver's cursor functionality.  
  
 If an application working with an ODBC 2*.x* driver makes calls to the ODBC 3.*x* cursor library, the application might be able to use ODBC 3.*x* features that are not supported by the ODBC 2*.x* driver. An application writer should be careful how these features are used, however. Use of the ODBC 3.*x* cursor library does not make an ODBC 2*.x* driver into an ODBC 3.*x* driver.