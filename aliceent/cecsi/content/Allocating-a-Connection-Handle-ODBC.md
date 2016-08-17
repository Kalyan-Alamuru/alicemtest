---
title: "Allocating a Connection Handle ODBC"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c99a8159-7693-4f97-8dcf-401336550e77
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Allocating a Connection Handle ODBC
Before the application can connect to a data source or driver, it must allocate a connection handle, as follows:  
  
1.  The application declares a variable of type SQLHDBC. It then calls **SQLAllocHandle** and passes the address of this variable, the handle of the environment in which to allocate the connection, and the SQL_HANDLE_DBC option. For example:  
  
    ```  
    SQLHDBC hdbc1;  
  
    SQLAllocHandle(SQL_HANDLE_DBC, henv1, &hdbc1);  
    ```  
  
2.  The Driver Manager allocates a structure in which to store information about the statement and returns the connection handle in the variable.  
  
 The Driver Manager does not call **SQLAllocHandle** in the driver at this time because it does not know which driver to call. It delays calling **SQLAllocHandle** in the driver until the application calls a function to connect to a data source. For more information, see [Driver Manager's Role in the Connection Process](../content/Driver-Manager-s-Role-in-the-Connection-Process.md), later in this section.  
  
 It is important to note that allocating a connection handle is not the same as loading a driver. The driver is not loaded until a connection function is called. Thus, after allocating a connection handle and before connecting to the driver or data source, the only functions the application can call with the connection handle are **SQLSetConnectAttr**, **SQLGetConnectAttr**, or **SQLGetInfo** with the SQL_ODBC_VER option. Calling other functions with the connection handle, such as **SQLEndTran**, returns SQLSTATE 08003 (Connection not open). For complete details, see [Appendix B: ODBC State Transition Tables](../Topic/Appendix%20B:%20ODBC%20State%20Transition%20Tables.md).  
  
 For more information about connection handles, see [Connection Handles](../content/Connection-Handles.md).