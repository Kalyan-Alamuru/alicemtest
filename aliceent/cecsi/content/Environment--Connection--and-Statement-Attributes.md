---
title: "Environment, Connection, and Statement Attributes"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9e15b276-3b7a-428a-b72f-a3ddfe1ba1ce
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Environment, Connection, and Statement Attributes
ODBC defines a number of attributes that are associated with environments, connections, or statements.  
  
 Environment attributes affect the entire environment, such as whether connection pooling is enabled. Environment attributes are set with **SQLSetEnvAttr** and retrieved with **SQLGetEnvAttr**.  
  
 Connection attributes affect each connection individually, such as how long a driver should wait while attempting to connect to a data source before timing out. Connection attributes are set with **SQLSetConnectAttr** and retrieved with **SQLGetConnectAttr**. For more information about connection attributes, see [Connection Attributes](../content/Connection-Attributes.md).  
  
 Statement attributes affect each statement individually, such as whether a statement should be executed asynchronously. Statement attributes are set with **SQLSetStmtAttr** and retrieved with **SQLGetStmtAttr**. A few statement attributes are read-only attributes and cannot be set. For example, the SQL_ATTR_ROW_NUMBER statement attribute, which is used to retrieve the number of the current row in the cursor, is read-only. For more information about statement attributes, see [Statement Attributes](../content/Statement-Attributes.md).  
  
 In addition to attributes defined by ODBC, a driver can define its own connection and statement attributes. Driver-defined attributes must be registered with Open Group to ensure that two driver vendors do not assign the same integer value to different, proprietary attributes. For more information, see [Driver-Specific Data Types, Descriptor Types, Information Types, Diagnostic Types, and Attributes](../content/Driver-Specific-Data-Types--Descriptor-Types--Information-Types--Diagnostic-Types--and-Attributes.md).  
  
 For a complete list of attributes, see [SQLSetEnvAttr](../content/SQLSetEnvAttr-Function.md), [SQLSetConnectAttr](../content/SQLSetConnectAttr-Function.md), and [SQLSetStmtAttr](../content/SQLSetStmtAttr-Function.md). Most attributes are also described in the description of the ODBC function that they affect.