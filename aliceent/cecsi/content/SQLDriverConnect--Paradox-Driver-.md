---
title: "SQLDriverConnect (Paradox Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c2ba486e-5e01-4e67-adb1-68511f5f0206
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLDriverConnect (Paradox Driver)
> [!NOTE]  
>  This topic provides Paradox Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 **SQLDriverConnect** enables you to connect to a driver without creating a data source (DSN).  
  
 The following keywords are supported in the connection string for all drivers: **DSN**, **DBQ**, and **FIL**.  
  
 The **PWD** keyword is also supported. The PWD keyword should not include any of the special characters (see SQL_SPECIAL_CHARACTERS in **SQLGetInfo** Returned Values).  
  
 After a password-protected file has been opened by a user, other users are not allowed to open the same file.  
  
 The following table shows the minimum keywords required to connect to each driver, and provides an example of keyword/value pairs used with **SQLDriverConnect**. For a full list of DRIVERID values, see [SQLConfigDataSource](../content/SQLConfigDataSource--Paradox-Driver-.md).  
  
> [!NOTE]  
>  If DBQ or DefaultDir is not specified for the Paradox driver, the driver will connect to the current directory.  
  
|Driver|Keywords required|Example|  
|------------|-----------------------|-------------|  
|Paradox|Driver, DriverID|Driver={Microsoft Paradox Driver (*.db )}; DBQ=c:\temp;DriverID=26|