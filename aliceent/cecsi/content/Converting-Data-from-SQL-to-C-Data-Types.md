---
title: "Converting Data from SQL to C Data Types"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 029727f6-d3f0-499a-911c-bcaf9714e43b
caps.latest.revision: 7
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Converting Data from SQL to C Data Types
When an application calls **SQLFetch**, **SQLFetchScroll**, or **SQLGetData**, the driver retrieves the data from the data source. If necessary, it converts the data from the data type in which the driver retrieved it to the data type specified by the *TargetType* argument in **SQLBindCol** or **SQLGetData.** Finally, it stores the data in the location pointed to by the *TargetValuePtr* argument in **SQLBindCol** or **SQLGetData** (and the SQL_DESC_DATA_PTR field of the ARD).  
  
 The following table shows the supported conversions from ODBC SQL data types to ODBC C data types. A filled circle indicates the default conversion for an SQL data type (the C data type to which the data will be converted when the value of *TargetType* is SQL_C_DEFAULT). A hollow circle indicates a supported conversion.  
  
 For an ODBC 3*.x* application working with an ODBC 2.*x* driver, conversion from driver-specific data types might not be supported.  
  
 The format of the converted data is not affected by the Windows® country setting.  
  
 The tables in the following sections describe how the driver or data source converts data retrieved from the data source; drivers are required to support conversions to all ODBC C data types from the ODBC SQL data types that they support. For a given ODBC SQL data type, the first column of the table lists the legal input values of the *TargetType* argument in **SQLBindCol** and **SQLGetData**. The second column lists the outcomes of a test, often using the *BufferLength* argument specified in **SQLBindCol** or **SQLGetData**, which the driver performs to determine whether it can convert the data. For each outcome, the third and fourth columns list the values placed in the buffers specified by the *TargetValuePtr* and *StrLen_or_IndPtr* arguments specified in **SQLBindCol** or **SQLGetData** after the driver has attempted to convert the data. (The *StrLen_or_IndPtr* argument corresponds to the SQL_DESC_OCTET_LENGTH_PTR field of the ARD.) The last column lists the SQLSTATE returned for each outcome by **SQLFetch**, **SQLFetchScroll**, or **SQLGetData**.  
  
 If the *TargetType* argument in **SQLBindCol** or **SQLGetData** contains an identifier for an ODBC C data type not shown in the table for a given ODBC SQL data type, **SQLFetch**, **SQLFetchScroll**, or **SQLGetData** returns SQLSTATE 07006 (Restricted data type attribute violation). If the *TargetType* argument contains an identifier that specifies a conversion from a driver-specific SQL data type to an ODBC C data type and this conversion is not supported by the driver, **SQLFetch**, **SQLFetchScroll**, or **SQLGetData** returns SQLSTATE HYC00 (Optional feature not implemented).  
  
 Although it is not shown in the tables, the driver returns SQL_NULL_DATA in the buffer specified by the *StrLen_or_IndPtr* argument when the SQL data value is NULL. For an explanation of the use of *StrLen_or_IndPtr* when multiple calls are made to retrieve data, see the [SQLGetData](../content/SQLGetData-Function.md)function description. When SQL data is converted to character C data, the character count returned in \**StrLen_or_IndPtr* does not include the null-termination byte. If *TargetValuePtr* is a null pointer, **SQLGetData** returns SQLSTATE HY009 (Invalid use of null pointer); in **SQLBindCol**, this unbinds the column.  
  
 The following terms and conventions are used in the tables:  
  
-   **Byte length of data** is the number of bytes of C data available to return in **TargetValuePtr*, whether or not the data will be truncated before it is returned to the application. For string data, this does not include the space for the null-termination character.  
  
-   **Character byte length** is the total number of bytes needed to display the data in character format. This is as defined for each C data type in the section [Display Size](../content/Display-Size.md), except that character byte length is in bytes while the display size is in characters.  
  
-   Words in *italics* represent function arguments or elements of the SQL grammar. For the syntax of grammar elements, see [Appendix C: SQL Grammar](../Topic/Appendix%20C:%20SQL%20Grammar.md).  
  
 This section contains the following topics.  
  
-   [SQL to C: Character](../Topic/SQL%20to%20C:%20Character.md)  
  
-   [SQL to C: Numeric](../Topic/SQL%20to%20C:%20Numeric.md)  
  
-   [SQL to C: Bit](../Topic/SQL%20to%20C:%20Bit.md)  
  
-   [SQL to C: Binary](../Topic/SQL%20to%20C:%20Binary.md)  
  
-   [SQL to C: Date](../Topic/SQL%20to%20C:%20Date.md)  
  
-   [SQL to C: GUID](../Topic/SQL%20to%20C:%20GUID.md)  
  
-   [SQL to C: Time](../Topic/SQL%20to%20C:%20Time.md)  
  
-   [SQL to C: Timestamp](../Topic/SQL%20to%20C:%20Timestamp.md)  
  
-   [SQL to C: Year-Month Intervals](../Topic/SQL%20to%20C:%20Year-Month%20Intervals.md)  
  
-   [SQL to C: Day-Time Intervals](../Topic/SQL%20to%20C:%20Day-Time%20Intervals.md)  
  
-   [SQL to C Data Conversion Examples](../content/SQL-to-C-Data-Conversion-Examples.md)