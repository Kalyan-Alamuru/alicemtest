---
title: "Block Cursors, Scrollable Cursors, and Backward Compatibility"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d9d271f6-d2d9-49b9-a365-4909ca06caae
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Block Cursors, Scrollable Cursors, and Backward Compatibility
The existence of both **SQLFetchScroll** and **SQLExtendedFetch** represents the first clear split in ODBC between the Application Programming Interface (API), which is the set of functions the application calls, and the Service Provider Interface (SPI), which is the set of functions the driver implements. This split is necessary so that ODBC 3.*x*, which uses **SQLFetchScroll**,bealigned with the standards and also be compatible with ODBC 2.*x*, which uses **SQLExtendedFetch**.  
  
 The ODBC 3*.x* API, which is the set of functions the application calls, includes **SQLFetchScroll** and related statement attributes. The ODBC 3*.x* SPI, which is the set of functions the driver implements, includes **SQLFetchScroll**, **SQLExtendedFetch**, and related statement attributes. Because ODBC does not formally enforce this split between the API and the SPI, it is possible for ODBC 3*.x* applications to call **SQLExtendedFetch** and related statement attributes. However, there is no reason for ODBC 3*.x* application to do this. For more information about APIs and SPIs, see the introduction to [ODBC Architecture](../content/ODBC-Architecture.md).  
  
 For information about what functions and statement attributes an ODBC 3.*x* application should use with block and scrollable cursors, see [Block Cursors, Scrollable Cursors, and Backward Compatibility for ODBC 3.x Applications](../content/Block-Cursors--Scrollable-Cursors--and-Backward-Compatibility-for-ODBC-3.x-Applications.md).  
  
 This section contains the following topics.  
  
-   [What the Driver Manager Does](../content/What-the-Driver-Manager-Does.md)  
  
-   [What the Driver Does](../content/What-the-Driver-Does.md)