---
title: "Data Type Conversions"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d311fe1c-d882-4136-9fa5-220a4121e04c
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Data Type Conversions
Data can be converted from one type to another at one of four times: when data is transferred from one application variable to another (C to C), when data in an application variable is sent to a statement parameter (C to SQL), when data in a result set column is returned in an application variable (SQL to C), and when data is transferred from one data source column to another (SQL to SQL).  
  
 Any conversion that occurs when data is transferred from one application variable to another is outside the scope of this document.  
  
 When an application binds a variable to a result set column or statement parameter, the application implicitly specifies a data type conversion in its choice of the data type of the application variable. For example, suppose a column contains integer data. If the application binds an integer variable to the column, it specifies that no conversion be done; if the application binds a character variable to the column, it specifies that the data be converted from integer to character.  
  
 ODBC defines how data is converted between each SQL and C data type. Basically, ODBC supports all reasonable conversions, such as character to integer and integer to float, and does not support ill-defined conversions, such as float to date. Drivers are required to support all conversions for each SQL data type they support. For a complete list of conversions between SQL and C data types, see [Converting Data from SQL to C Data Types](../content/Converting-Data-from-SQL-to-C-Data-Types.md) and [Converting Data from C to SQL Data Types](../content/Converting-Data-from-C-to-SQL-Data-Types.md) in Appendix D: Data Types.  
  
 ODBC also defines a scalar function for converting data from one SQL data type to another. The **CONVERT** scalar function is mapped by the driver to the underlying scalar function or functions defined to perform conversions in the data source. Because this function is mapped to DBMS-specific functions, ODBC does not define how these conversions work or what conversions must be supported. An application discovers what conversions are supported by a particular driver and data source through the SQL_CONVERT options in **SQLGetInfo**. For more information about the **CONVERT** scalar function, see [Escape Sequences in ODBC](../content/Escape-Sequences-in-ODBC.md) and [Explicit Data Type Conversion Function](../content/Explicit-Data-Type-Conversion-Function.md).