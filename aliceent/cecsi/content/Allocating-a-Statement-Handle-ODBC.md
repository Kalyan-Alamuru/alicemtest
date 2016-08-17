---
title: "Allocating a Statement Handle ODBC"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4ce3b446-34ab-46dc-96e5-f40ec95c267e
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Allocating a Statement Handle ODBC
Before the application can execute a statement, it must allocate a statement handle as follows:  
  
1.  The application declares a variable of type HSTMT. It then calls **SQLAllocHandle** and passes the address of this variable, the handle of the connection in which to allocate the statement, and the SQL_HANDLE_STMT option. For example:  
  
    ```  
    SQLHSTMT hstmt1;  
  
    SQLAllocHandle(SQL_HANDLE_STMT, hdbc1, &hstmt1);  
    ```  
  
2.  The Driver Manager allocates a structure in which to store information about the statement and calls **SQLAllocHandle** in the driver with the SQL_HANDLE_STMT option.  
  
3.  The driver allocates its own structure in which to store information about the statement and returns the driver statement handle to the Driver Manager.  
  
4.  The Driver Manager returns the Driver Manager statement handle to the application in the application variable.  
  
 The statement handle identifies which statement to use when calling ODBC functions. For more information about statement handles, see [Statement Handles](../content/Statement-Handles.md).