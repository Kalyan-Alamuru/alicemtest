---
title: "Appendix E: Scalar Functions"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 59c7cd5e-32d6-43ab-bac3-7010322d105a
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Appendix E: Scalar Functions
ODBC specifies the following types of scalar functions, with detailed information about each of these function types provided in the corresponding sections of this appendix. The function descriptions include associated syntax.  
  
 This appendix contains the following topics.  
  
-   [String Functions](../content/String-Functions.md)  
  
-   [Numeric Functions](../content/Numeric-Functions.md)  
  
-   [Time, Date, and Interval Functions](../content/Time--Date--and-Interval-Functions.md)  
  
-   [System Functions](../content/System-Functions.md)  
  
-   [Explicit Data Type Conversion Function](../content/Explicit-Data-Type-Conversion-Function.md)  
  
-   [SQL-92 CAST Function](../content/SQL-92-CAST-Function.md)  
  
 ODBC does not mandate a data type for return values from scalar functions because the functions are often data source–specific. Applications should use the CONVERT scalar function whenever possible to force data type conversion.  
  
## ODBC and SQL-92 Scalar Functions  
 The tables in this appendix include functions that have been added in ODBC 3.0 to align with SQL-92. Those functions added for a particular type of scalar function, as defined in ODBC, are indicated in each section.  
  
 ODBC and SQL-92 classify their scalar functions differently. ODBC classifies scalar functions by argument type; SQL-92 classifies them by return value. For example, the EXTRACT function is classified as a timedate function by ODBC, because the extract-field argument is a datetime keyword and the extract-source argument is a datetime or interval expression. SQL-92, on the other hand, classifies EXTRACT as a numeric scalar function, because the return value is a numeric.  
  
 An application can determine which scalar functions a driver supports by calling **SQLGetInfo**. Information types are included both for ODBC and for SQL-92 classifications of scalar functions. Because these classifications are different, the support for some scalar functions may be indicated in information types that do not correspond to ODBC and SQL-92. For example, support for EXTRACT in ODBC is indicated by the SQL_TIMEDATE_FUNCTIONS information type; support for EXTRACT in SQL-92, on the other hand, is indicated by the SQL_SQL92_NUMERIC_VALUE_FUNCTIONS information type.