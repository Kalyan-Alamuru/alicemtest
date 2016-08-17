---
title: "Catalog Functions in ODBC"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4f28f557-7eca-4905-aa6d-45a6cf501a66
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Catalog Functions in ODBC
ODBC contains the following catalog functions:  
  
|Function|Description|  
|--------------|-----------------|  
|**SQLTables**|Returns a list of catalogs, schemas, tables, or table types in the data source.|  
|**SQLColumns**|Returns a list of columns in one or more tables.|  
|**SQLStatistics**|Returns a list of statistics about a single table. Also returns a list of indexes associated with that table.|  
|**SQLSpecialColumns**|Returns a list of columns that uniquely identifies a row in a single table. Also returns a list of columns in that table that are automatically updated.|  
|**SQLPrimaryKeys**|Returns a list of columns that compose the primary key of a single table.|  
|**SQLForeignKeys**|Returns a list of foreign keys in a single table or a list of foreign keys in other tables that refer to a single table.|  
|**SQLTablePrivileges**|Returns a list of privileges associated with one or more tables.|  
|**SQLColumnPrivileges**|Returns a list of privileges associated with one or more columns in a single table.|  
|**SQLProcedures**|Returns a list of procedures in the data source.|  
|**SQLProcedureColumns**|Returns a list of input and output parameters, the return value, and the columns in the result set of a single procedure.|  
|**SQLGetTypeInfo**|Returns a list of the SQL data types supported by the data source. These data types are generally used in **CREATE TABLE** and **ALTER TABLE** statements.|  
  
 Because **SQLTables**, **SQLColumns**, **SQLStatistics**, and **SQLSpecialColumns** conform to the Open Group CLI, and **SQLGetTypeInfo** conforms to the ISO 92 CLI, they are implemented by most drivers. The remaining catalog functions are in the ODBC conformance level.  
  
 This section contains the following topics.  
  
-   [Data Returned by Catalog Functions](../content/Data-Returned-by-Catalog-Functions.md)  
  
-   [Arguments in Catalog Functions](../content/Arguments-in-Catalog-Functions.md)  
  
-   [Schema Views](../content/Schema-Views.md)