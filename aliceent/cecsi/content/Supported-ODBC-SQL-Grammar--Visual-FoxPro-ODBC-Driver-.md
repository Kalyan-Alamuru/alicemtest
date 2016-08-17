---
title: "Supported ODBC SQL Grammar (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f41a38c2-e22e-4c65-a32e-9a6777435160
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Supported ODBC SQL Grammar (Visual FoxPro ODBC Driver)
The Microsoft Visual FoxPro ODBC Driver supports the following:  
  
-   All SQL statements and clauses in the ODBC minimum SQL grammar  
  
-   An additional SQL statement from the ODBC core SQL grammar  
  
 The following table lists the items supported by the driver, by ODBC SQL Grammar level.  
  
|Level|Elements|Item|  
|-----------|--------------|----------|  
|Minimum|Data Definition Language (DDL)|CREATE TABLE and DROP TABLE|  
||Data Manipulation Language (DML)|SELECT, INSERT, UPDATE, and DELETE|  
||Expressions|Simple (such as A>B+C)|  
||Data types|CHAR, VARCHAR, or LONG VARCHAR|  
  
 In addition to the supported ODBC SQL grammar, the Visual FoxPro ODBC Driver supports the complete native Visual FoxPro language syntax for the following Visual FoxPro commands:  
  
 [ALTER TABLE](../content/ALTER-TABLE---SQL-Command.md)  
  
 [CREATE TABLE](../content/CREATE-TABLE---SQL-Command.md)  
  
 [DELETE](../content/DELETE---SQL-Command.md)  
  
 [DELETE TAG](../content/DELETE-TAG-Command.md)  
  
 [DROP TABLE](../content/DROP-TABLE-Command.md)  
  
 [INDEX](../content/INDEX-Command.md)  
  
 [INSERT](../content/INSERT---SQL-Command.md)  
  
 [SELECT](../content/SELECT---SQL-Command.md)  
  
 [UPDATE](../content/UPDATE---SQL-Command.md)