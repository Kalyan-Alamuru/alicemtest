---
title: "Step 1: Connect to the Data Source"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 84298664-4523-4149-b821-7b2e42c85281
caps.latest.revision: 8
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Step 1: Connect to the Data Source
The first step in any application is to connect to the data source. This phase, including the functions it requires, is shown in the following illustration.  
  
 ![Connecting to the data source in an ODBC app](../content/media/pr11.gif "pr11")  
  
 The first step in connecting to the data source is to load the Driver Manager and allocate the environment handle with **SQLAllocHandle**. For more information, see [Allocating the Environment Handle](../content/Allocating-the-Environment-Handle.md).  
  
 The application then registers the version of ODBC to which it conforms by calling **SQLSetEnvAttr** with the SQL_ATTR_APP_ODBC_VER environment attribute. For more information, see [Declaring the Application's ODBC Version](../content/Declaring-the-Application-s-ODBC-Version.md) and [Backward Compatibility and Standards Compliance](../content/Backward-Compatibility-and-Standards-Compliance.md).  
  
 Next, the application allocates a connection handle with **SQLAllocHandle** and connects to the data source with **SQLConnect**, **SQLDriverConnect**, or **SQLBrowseConnect**. For more information, see [Allocating a Connection Handle](../content/Allocating-a-Connection-Handle-ODBC.md) and [Establishing a Connection](../content/Establishing-a-Connection.md).  
  
 The application then sets any connection attributes, such as whether to manually commit transactions. For more information, see [Connection Attributes](../content/Connection-Attributes.md).