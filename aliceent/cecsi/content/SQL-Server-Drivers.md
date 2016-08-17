---
title: "SQL Server Drivers"
ms.custom: na
ms.date: 08/17/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a5a9e591-4236-4105-9464-70cd36eeeb51
caps.latest.revision: 12
manager: jhubbard
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pt-br
  - ru-ru
  - zh-cn
  - zh-tw
---
# SQL Server Drivers
SQL Server supports a wide variety of drivers, which are used by client applications or services to connect and query for data.  Please see below for a summary of the different drivers, both current and legacy.  
  
## Current SQL Drivers  
 The following SQL Drivers are actively developed. Each driver has a support statement that can be found by following the links.  
  
### ADO.NET  
 ADO.NET is a library that is a standard part of the .Net framework.  It is a C# implementation of the TDS protocol, which is supported by all modern versions of SQL Server.    
                          This driver is developed, tested, and supported by Microsoft.  
  
 [Microsoft ADO.NET for SQL Server](../content/Microsoft-ADO.NET-for-SQL-Server.md)  
  
### JDBC  
 The JDBC SQL driver is a Java implementation of the TDS protocol, which is supported by all modern versions of SQL Server.  This driver is developed, tested, and supported by Microsoft.  
  
 [Microsoft JDBC Driver for SQL Server](../content/Microsoft-JDBC-Driver-for-SQL-Server.md)  
  
### ODBC  
 The ODBC SQL driver is a C++ implementation of the TDS protocol, which is supported by all modern versions of SQL Server.  This driver is developed, tested, and supported by Microsoft.  
  
 [Microsoft ODBC Driver for SQL Server](../content/Microsoft-ODBC-Driver-for-SQL-Server.md)  
  
### PHP  
 The PHP SQL driver relies on the Microsoft SQL Server ODBC Driver to handle the low-level communication with SQL Server.  This driver is developed, tested, and supported by Microsoft.  
  
 [Microsoft PHP Driver for SQL Server](../content/Microsoft-PHP-Driver-for-SQL-Server.md)  
  
### Node.js  
 The tedious module is a javascript implementation of the TDS protocol, which is supported by all modern versions of SQL Server.  The driver is an open source project, available on Github.  
  
 [Node.js Driver for SQL Server](../content/Node.js-Driver-for-SQL-Server.md)  
  
### Python  
 The pymssql module is a Python implementation of the TDS protocol, which is supported by all modern versions of SQL Server.  
  
 [Python Driver for SQL Server](../content/Python-Driver-for-SQL-Server.md)  
  
### Ruby  
 The TinyTDS gem is a Ruby implementation of the TDS protocol, which is supported by all modern versions of SQL Server.  
  
 [Ruby Driver for SQL Server](../content/Ruby-Driver-for-SQL-Server.md)  
  
## Legacy SQL Drivers  
 The following SQL Drivers were developed and tested by Microsoft, but are not recommended to be used for new development. Each driver has a support statement that can be found by following the links.  
  
### OLEDB  
 The OLE DB provider will not be included after SQL Server 2012.  
  
 [Microsoft OLE DB](https://msdn.microsoft.com/library/ms722784.aspx)  
  
### ADO  
 The ADO SQL driver has a direct dependency on the OLE DB provider.  As such, it will not be supported after SQL Server 2012.  
  
 [ActiveX Data Objects (ADO)](../content/ActiveX-Data-Objects--ADO-.md)