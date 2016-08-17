---
title: "Fixed-Length Bookmarks"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cbd8185e-fb03-408f-b80b-1a2e164534fd
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Fixed-Length Bookmarks
If an ODBC 3*.x* driver should work with an ODBC 2.*x* application that uses fixed-length bookmarks, the driver must support the following:  
  
-   SQL_UB_ON as a value for the SQL_USE_BOOKMARKS statement option. (SQL_UB_ON is deprecated in ODBC 3*.x*.)  
  
-   The SQL_GET_BOOKMARK statement option.