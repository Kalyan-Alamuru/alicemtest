---
title: "Cursor Library Cache"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d6a91cd6-3905-4e3a-98ab-37fce893dbe1
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Cursor Library Cache
> [!IMPORTANT]  
>  This feature will be removed in a future version of Windows. Avoid using this feature in new development work and plan to modify applications that currently use this feature. Microsoft recommends using the driver's cursor functionality.  
  
 For each row of data in the result set, the cursor library caches the data for each bound column, the length of the data in each bound column, and the status of the row. The cursor library uses the values in the cache both to return through **SQLFetch** and **SQLFetchScroll** and to construct searched statements for positioned operations. For more information, see [Constructing Searched Statements](../content/Constructing-Searched-Statements.md).  
  
 This section contains the following topics.  
  
-   [Column Data](../content/Column-Data.md)  
  
-   [Length of Column Data](../content/Length-of-Column-Data.md)  
  
-   [Row Status](../content/Row-Status.md)  
  
-   [Location of Cache](../content/Location-of-Cache.md)