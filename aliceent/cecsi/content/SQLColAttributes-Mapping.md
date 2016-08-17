---
title: "SQLColAttributes Mapping"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 30e25719-176b-4c48-97d4-920766b22412
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLColAttributes Mapping
When an application calls **SQLColAttributes** through an ODBC 3*.x* driver, the call to **SQLColAttributes** is mapped to **SQLColAttribute** as follows:  
  
> [!NOTE]  
>  The prefix used in *FieldIdentifier* values in ODBC 3*.x* has been changed from that used in ODBC 2.*x*. The new prefix is "SQL_DESC"; the old prefix was "SQL_COLUMN".  
  
1.  If the application is an ODBC 2.*x* application, *fDescType* is SQL_COLUMN_TYPE, and the returned type is a concise DATETIME type, the Driver Manager maps the return values for date, time, and timestamp codes.  
  
2.  If *fDescType* is SQL_COLUMN_NAME, SQL_COLUMN_NULLABLE, or SQL_COLUMN_COUNT, the Driver Manager calls **SQLColAttribute** in the driver with the *FieldIdentifier* argument mapped to SQL_DESC_NAME, SQL_DESC_NULLABLE, or SQL_DESC_COUNT, as appropriate*.* All other values of *fDescType* are passed through to the driver.  
  
 An ODBC 3*.x* driver must support all the ODBC 3*.x* *FieldIdentifiers* listed for **SQLColAttribute**.  
  
 An ODBC 3*.x* driver must support SQL_COLUMN_PRECISION and SQL_DESC_PRECISION, SQL_COLUMN_SCALE and SQL_DESC_SCALE, and SQL_COLUMN_LENGTH and SQL_DESC_LENGTH. These values are different because precision, scale, and length are defined differently in ODBC 3*.x* than they were in ODBC 2.*x*. For more information, see [Column Size, Decimal Digits, Transfer Octet Length, and Display Size](../content/Column-Size--Decimal-Digits--Transfer-Octet-Length--and-Display-Size.md) in Appendix D: Data Types.