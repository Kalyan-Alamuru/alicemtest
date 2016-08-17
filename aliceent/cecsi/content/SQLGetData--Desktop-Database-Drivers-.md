---
title: "SQLGetData (Desktop Database Drivers)"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c9d9a32d-5dc2-4189-9bfb-2b008bc3d6a3
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLGetData (Desktop Database Drivers)
This function can retrieve data from any column, whether or not there are bound columns after it and regardless of the order in which the columns are retrieved.  
  
> [!NOTE]  
>  \*pcbValue in **SQLGetData** may return twice as many characters as actually available when binding to ANSI data longer than 510 characters on a Jet 4.0 database. Character values of 510 or less will return the actual cbValue.