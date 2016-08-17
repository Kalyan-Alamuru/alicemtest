---
title: "SQLDriverConnect (Access Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9d133e9b-7545-464d-aa3c-677fa7e2a41d
caps.latest.revision: 7
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLDriverConnect (Access Driver)
> [!NOTE]  
>  This topic provides Access Driver-specific information. For general information about this function, see the appropriate topic under [ODBC API Reference](../content/ODBC-API-Reference.md).  
  
 **SQLDriverConnect** enables you to connect to a driver without creating a data source (DSN).  
  
 The following keywords are supported in the connection string for all drivers: **DSN**, **DBQ**, and **FIL**.  
  
 The **UID** and **PWD** keywords are also supported.  
  
 The PWD keyword should not include any of the special characters (see SQL_SPECIAL_CHARACTERS in **SQLGetInfo** Returned Values).  
  
 The following table shows the minimum keywords required to connect to each driver, and provides an example of keyword/value pairs used with **SQLDriverConnect**. For a full list of DRIVERID values, see [SQLConfigDataSource](../content/SQLConfigDataSource--Access-Driver-.md).  
  
|Driver|Keywords Required|Examples|  
|------------|-----------------------|--------------|  
|Microsoft Access|Driver, DBQ|Driver={Microsoft Access Driver (*.mdb)}; DBQ=c:\\\temp\\\sample.mdb|