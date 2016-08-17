---
title: "SQLAllocEnv Mapping"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4bb51845-ee91-4b97-9dd4-2fab977f2aec
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLAllocEnv Mapping
When an application calls **SQLAllocEnv** through an ODBC 3*.x* driver, the call to **SQLAllocEnv**(*phenv*) is mapped to **SQLAllocHandle** as follows:  
  
1.  The Driver Manager allocates an environment handle and returns it to the application. The Driver Manager calls **SQLSetEnvAttr** to set the SQL_ATTR_ODBC_VERSION environment attribute to SQL_OV_ODBC2.  
  
2.  When the application establishes the first connection to a driver, the Driver Manager calls  
  
    ```  
    SQLAllocHandle(SQL_HANDLE_ENV, SQL_NULL_HANDLE, OutputHandlePtr)  
    ```  
  
     in the driver with *OutputHandlePtr* set to *phenv*.