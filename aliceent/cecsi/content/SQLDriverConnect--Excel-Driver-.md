---
title: "SQLDriverConnect (Excel Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 285cb1ea-f461-4596-97f2-fc57af05dede
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLDriverConnect (Excel Driver)
> [!NOTE]  
>  This topic provides Excel Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 **SQLDriverConnect** enables you to connect to a driver without creating a data source (DSN).  
  
 The following keywords are supported in the connection string for all drivers: **DSN**, **DBQ**, and **FIL**.  
  
 The following table shows the minimum keywords required to connect to each driver, and provides an example of keyword/value pairs used with **SQLDriverConnect**. For a full list of DRIVERID values, see [SQLConfigDataSource](../content/ODBC-Jet-SQLConfigDataSource--Excel-Driver-.md).  
  
> [!NOTE]  
>  If DBQ or DefaultDir is not specified for the Microsoft Excel 3.0 or 4.0 driver, the driver will connect to the current directory.  
  
|Driver|Keywords Required|Examples|  
|------------|-----------------------|--------------|  
|Microsoft Excel 3.0 or 4.0|Driver, DriverID|Driver={Microsoft Excel Driver (*.xls)}; DBQ=c:\temp; DriverID=278|  
|Microsoft Excel 5.0/7.0|Driver, DriverID,  DBQ|Driver={Microsoft Excel Driver (*.xls)}; DBQ=c:\temp\sample.xls; DriverID=22|  
|Microsoft Excel 97 and later|Driver, DriverID,  DBQ|Driver={Microsoft Excel Driver (*.xls)}; DBQ=c:\temp\sample.xls; DriverID=790|