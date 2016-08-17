---
title: "SQLFreeConnect Mapping"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8a844538-93c0-4709-bab6-35c45e771d80
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLFreeConnect Mapping
When an application calls **SQLFreeConnect** through an ODBC 3*.x* driver, the call to  
  
```  
SQLFreeConnect(hdbc)   
```  
  
 is mapped to  
  
```  
SQLFreeHandle(SQL_HANDLE_DBC,Handle)  
```  
  
 with the *Handle* argument set to the value in *hdbc*.