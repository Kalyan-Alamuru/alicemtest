---
title: "Connecting Directly to Drivers"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f86e198f-a088-4401-9106-aa62a0eb8f6e
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Connecting Directly to Drivers
As was discussed in [Choosing a Data Source or Driver](../content/Choosing-a-Data-Source-or-Driver.md), earlier in this section, some applications do not want to use a data source at all. Instead, they want to connect directly to a driver. **SQLDriverConnect** provides a way for the application to connect directly to a driver without specifying a data source. Conceptually, a temporary data source is created at run time.  
  
 To connect directly to a driver, the application specifies the **DRIVER** keyword in the connection string instead of the **DSN** keyword. The value of the **DRIVER** keyword is the description of the driver as returned by **SQLDrivers**. For example, suppose a driver has the description Paradox Driver and requires the name of a directory containing the data files. To connect to this driver, the application might use either of the following connection strings:  
  
```  
DRIVER={Paradox Driver};Directory=C:\PARADOX;  
DRIVER={Paradox Driver};  
```  
  
 With the first string, the driver would not need any additional information. With the second string, the driver would need to prompt for the name of the directory containing the data files.