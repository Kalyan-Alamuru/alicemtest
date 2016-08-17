---
title: "SQLAllocConnect Mapping"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ac89dd1f-c565-47cc-8fa3-6fa5f80b5d63
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLAllocConnect Mapping
When an application calls **SQLAllocConnect** through an ODBC 3.*x* driver, the call to **SQLAllocConnect**(*henv*, *phdbc*) is mapped to **SQLAllocHandle** as follows:  
  
1.  The Driver Manager allocates a connection and returns it to the application.  
  
2.  When the application establishes a connection, the Driver Manager calls  
  
    ```  
    SQLAllocHandle(SQL_HANDLE_DBC, InputHandle, OutputHandlePtr)  
    ```  
  
     in the driver with *InputHandle* set to *henv*, and *OutputHandlePtr* set to *phdbc*.