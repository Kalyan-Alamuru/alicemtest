---
title: "Default Data Source"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dd473cc6-f051-4aa0-ab14-3dd1b37fe99e
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Default Data Source
The driver may select a data source, called the default data source, in certain cases where the application does not explicitly specify one:  
  
-   In a call to **SQLConnect** where the *ServerName* argument is a zero-length string, a null pointer, or DEFAULT.  
  
-   In a call to **SQLDriverConnect** where *InConnectionString* either specifies **DSN**=DEFAULT or specifies with the **DSN** keyword a data source that is not contained in the system information.  
  
 It is driver-defined how the default data source is specified. This may involve administrative action and may depend on the user.