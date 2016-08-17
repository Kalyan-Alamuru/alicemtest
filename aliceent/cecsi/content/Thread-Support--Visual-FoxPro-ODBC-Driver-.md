---
title: "Thread Support (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0c6abbbc-012b-41aa-bded-5e7e362d015b
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Thread Support (Visual FoxPro ODBC Driver)
The Visual FoxPro ODBC Driver is thread-safe. Access to environment handles (*hen*), connection handles (*hdbc*), and statement handles (*hstmt*) is wrapped in appropriate semaphores to prevent other processes from accessing and potentially altering the driver's internal data structures.  
  
 In a multithreaded application, you can cancel a function that is running synchronously on an *hstmt* by calling [SQLCancel](../content/SQLCancel--Visual-FoxPro-ODBC-Driver-.md) on a separate thread.  
  
 The driver uses a separate thread to fetch data when you use progressive fetching. To use progressive fetching for a data source, select the **Fetch data in background** check box on the [ODBC Visual FoxPro Setup dialog box](../content/ODBC-Visual-FoxPro-Setup-Dialog-Box.md) or use the BackgroundFetch attribute keyword in your connection string. Avoid using background fetch when you call the driver from multithreaded applications. For information about connection string attribute keywords, see [Using Connection Strings](../content/Using-Connection-Strings.md).  
  
 For more information about threads and **SQLCancel**, see [SQLCancel](../content/SQLCancel-Function.md) in the *ODBC Programmer's Reference*.