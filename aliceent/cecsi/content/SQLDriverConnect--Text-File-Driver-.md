---
title: "SQLDriverConnect (Text File Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d7769021-bd18-4d8e-96e0-e184a82d6ca3
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLDriverConnect (Text File Driver)
> [!NOTE]  
>  This topic provides Text File Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 **SQLDriverConnect** enables you to connect to a driver without creating a data source (DSN).  
  
 The following keywords are supported in the connection string for all drivers: **DSN**, **DBQ**, and **FIL**.  
  
 The following table shows the minimum keywords required to connect to each driver, and provides an example of keyword/value pairs used with **SQLDriverConnect**. For a full list of DRIVERID values, see [SQLConfigDataSource](../content/SQLConfigDataSource--Text-File-Driver-.md).  
  
> [!NOTE]  
>  If DBQ or DefaultDir is not specified for the Text driver, the driver will connect to the current directory.  
  
|Driver|Keywords required|Examples|  
|------------|-----------------------|--------------|  
|Text|Driver|Driver={Microsoft Text Driver (*.txt;\*.csv)}; DefaultDir=c:\temp|