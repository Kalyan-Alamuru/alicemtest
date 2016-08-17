---
title: "C Data Types in ODBC"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c91bef31-3794-4736-966a-d50997b2233c
caps.latest.revision: 26
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# C Data Types in ODBC
ODBC defines the C data types that are used by application variables and their corresponding type identifiers. These are used by the buffers that are bound to result set columns and statement parameters. For example, suppose an application wants to retrieve data from a result set column in character format. It declares a variable with the SQLCHAR * data type and binds this variable to the result set column with a type identifier of SQL_C_CHAR. For a complete list of C data types and type identifiers, see [Appendix D: Data Types](../Topic/Appendix%20D:%20Data%20Types.md).  
  
 ODBC also defines a default mapping from each SQL data type to a C data type. For example, a 2-byte integer in the data source is mapped to a 2-byte integer in the application. To use the default mapping, an application specifies the SQL_C_DEFAULT type identifier. However, use of this identifier is discouraged for interoperability reasons.  
  
 All integer C data types defined in ODBC 1*.x* were signed. Unsigned C data types and their corresponding type identifiers were added in ODBC 2.0. Because of this, applications and drivers need to be particularly careful when dealing with 1*.x* versions.  
  
## C Data Type Extensibility  
 In ODBC 3.8, you can specify driver-specific C data types. This enables you to bind a SQL type as a driver-specific C type in ODBC applications when you call [SQLBindCol](../content/SQLBindCol-Function.md), [SQLGetData](../content/SQLGetData-Function.md), or [SQLBindParameter](../content/SQLBindParameter-Function.md). This can be useful for supporting new server types, because existing C data types might not correctly represent the new server data types. Using driver-specific C types can increase the number of conversions that drivers can perform.  
  
 For example, suppose a database management system (DBMS) introduced a new SQL type, **DATETIMEOFFSET**, to represent the date and time with time zone information. There would be no specific C type in ODBC that corresponded to **DATETIMEOFFSET**. An application would have to bind **DATETIMEOFFSET** as SQL_C_BINARY and cast it to a user-defined data type. Beginning in ODBC 3.8 with C data type extensibility, a driver can define a new corresponding C type. For example, for the new SQL type DATETIMEOFFSET, the driver can define a new corresponding C type such as SQL_C_DATETIMEOFFSET. Then, an application can bind the new SQL type as a driver-specific C type.  
  
 A C data type is defined in the driver as follows:  
  
-   The ODBC compliance level for an application, ODBC driver, and Driver Manager is 3.8 (or higher).  
  
-   The data range of a driver-specific C type is between 0x4000 and 0x7FFF.  
  
-   The driver defines the structure of the data corresponding to the C type.  This can be done in the driver-specific SDK.  
  
 The driver manager will not validate a C type defined in the range of 0x4000 and 0x7FFF; the driver will perform the validation and any data type conversion. But if the data range of a C type passed to the driver manager is between 0x0000 and 0x3FFF or between 0x8000 and 0xFFFF, the driver manager will validate the C data type.  
  
> [!NOTE]  
>  Driver-specific C data types should be described in the driver documentation.  
  
 To specify an ODBC compliance level of 3.8, an application calls [SQLSetEnvAttr](../content/SQLSetEnvAttr-Function.md) with the SQL_ATTR_ODBC_VERSION attribute set to **SQL_OV_ODBC3_80**. To determine the version of the driver, an application calls **SQLGetInfo** with SQL_DRIVER_ODBC_VER.  
  
 For more information about ODBC 3.8, see [What's New in ODBC 3.8](../content/What-s-New-in-ODBC-3.8.md).  
  
## See Also  
 [C Data Types](../content/C-Data-Types.md)