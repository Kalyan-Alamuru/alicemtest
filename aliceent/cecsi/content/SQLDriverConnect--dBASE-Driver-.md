---
title: "SQLDriverConnect (dBASE Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c837aa31-068e-4fa3-bc00-aae09bec21de
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLDriverConnect (dBASE Driver)
> [!NOTE]  
>  This topic provides dBASE Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 **SQLDriverConnect** enables you to connect to a driver without creating a data source (DSN).  
  
 The following keywords are supported in the connection string for all drivers: **DSN**, **DBQ**, and **FIL**.  
  
 When the Paradox driver is used, after a password-protected file has been opened by a user, other users are not allowed to open the same file.  
  
 The following table shows the minimum keywords required to connect to each driver, and provides an example of keyword/value pairs used with **SQLDriverConnect**. For a full list of DRIVERID values, see [SQLConfigDataSource](../content/SQLConfigDataSource--dBASE-Driver-.md).  
  
> [!NOTE]  
>  If DBQ or DefaultDir is not specified for the dBASEdriver, the driver will connect to the current directory.  
  
|Driver|Keywords required|Examples|  
|------------|-----------------------|--------------|  
|dBASE|Driver, DriverID|Driver={Microsoft dBASE Driver (*.dbf)}; DBQ=c:\temp; DriverID=277|