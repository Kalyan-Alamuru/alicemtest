---
title: "Appendix D: Data Types"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 981d49c3-3531-4543-aa75-5bd9e4f67000
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Appendix D: Data Types
ODBC defines two sets of data types: SQL data types and C data types. SQL data types indicate the data type of data stored at the data source. C data types indicate the data type of data stored in application buffers.  
  
 SQL data types are defined by each DBMS in accordance with the SQL-92 standard. For each SQL data type specified in the SQL-92 standard, ODBC defines a type identifier, which is a **#define** value that is passed as an argument in ODBC functions or returned in the metadata of a result set. The only SQL-92 data types not supported by ODBC are BIT (the ODBC SQL_BIT type has different characteristics), BIT_VARYING, TIME_WITH_TIMEZONE, TIMESTAMP_WITH_TIMEZONE, and NATIONAL_CHARACTER. Drivers are responsible for mapping data source–specific SQL data types to ODBC SQL data type identifiers and driver-specific SQL data type identifiers. The SQL data type is specified in the SQL_DESC_CONCISE_TYPE field of an implementation descriptor.  
  
 ODBC defines the C data types and their corresponding ODBC type identifiers. An application specifies the C data type of the buffer that will receive result set data by passing the appropriate C type identifier in the *TargetType* argument in a call to **SQLBindCol** or **SQLGetData**. It specifies the C type of the buffer containing a statement parameter by passing the appropriate C type identifier in the *ValueType* argument in a call to **SQLBindParameter**. The C data type is specified in the SQL_DESC_CONCISE_TYPE field of an application descriptor.  
  
> [!NOTE]  
>  There are no driver-specific C data types.  
  
 Each SQL data type corresponds to an ODBC C data type. Before returning data from the data source, the driver converts it to the specified C data type. Before sending data to the data source, the driver converts it from the specified C data type.  
  
 This appendix contains the following topics.  
  
-   [Using Data Type Identifiers](../content/Using-Data-Type-Identifiers.md)  
  
-   [SQL Data Types](../content/SQL-Data-Types.md)  
  
-   [C Data Types](../content/C-Data-Types.md)  
  
-   [Data Type Identifiers and Descriptors](../content/Data-Type-Identifiers-and-Descriptors.md)  
  
-   [Pseudo-Type Identifiers](../content/Pseudo-Type-Identifiers.md)  
  
-   [Transferring Data in Its Binary Form](../content/Transferring-Data-in-Its-Binary-Form.md)  
  
-   [Guidelines for Interval and Numeric Data Types](../content/Guidelines-for-Interval-and-Numeric-Data-Types.md)  
  
-   [Constraints of the Gregorian Calendar](../content/Constraints-of-the-Gregorian-Calendar.md)  
  
-   [Column Size, Decimal Digits, Transfer Octet Length, and Display Size](../content/Column-Size--Decimal-Digits--Transfer-Octet-Length--and-Display-Size.md)  
  
-   [Converting Data from SQL to C Data Types](../content/Converting-Data-from-SQL-to-C-Data-Types.md)  
  
-   [Converting Data from C to SQL Data Types](../content/Converting-Data-from-C-to-SQL-Data-Types.md)  
  
 For an explanation of ODBC data types, see [Data Types in ODBC](../content/Data-Types-in-ODBC.md). For information about driver-specific SQL data types, see the driver's documentation.