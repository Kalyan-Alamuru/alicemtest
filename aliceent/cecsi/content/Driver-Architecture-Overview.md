---
title: "Driver Architecture Overview"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ef5a91cd-158e-40bf-b5a8-8ba535c4705e
caps.latest.revision: 7
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Driver Architecture Overview
The Microsoft Visual FoxPro ODBC Driver is a 32-bit driver that enables you to open and query a Microsoft Visual FoxPro database or FoxPro tables through the Open Database Connectivity (ODBC) interface. You can access FoxPro data using the following types of applications:  
  
-   A Microsoft Office application, such as Microsoft Excel or Microsoft Word, that uses Microsoft Query to communicate with ODBC.  
  
-   An application written in Microsoft Visual C++ or C that uses the ODBC SDK API.  
  
-   An application written in Microsoft Visual Basic or Microsoft Visual Basic for Applications.  
  
 In each case, the request for information uses the ODBC API. The ODBC Driver Manager works with the Visual FoxPro ODBC Driver to open and retrieve data from FoxPro tables and databases.  
  
 The architecture is represented in the following diagram:  
  
 ![Shows the ODBC Driver architecture](../content/media/vfparch.gif "vfparch")  
  
 This section contains the following topics.  
  
-   [Visual FoxPro Terminology](../content/Visual-FoxPro-Terminology.md)  
  
-   [Installing and Configuring the Visual FoxPro ODBC Driver](../content/Installing-and-Configuring.md)  
  
-   [Using the Visual FoxPro ODBC Driver](../content/Using-the-Visual-FoxPro-ODBC-Driver.md)