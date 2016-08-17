---
title: "ODBC Overview"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 233315bd-2b7f-4b20-9978-e920e1ea9a07
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# ODBC Overview
Open Database Connectivity (ODBC) is a widely accepted application programming interface (API) for database access. It is based on the Call-Level Interface (CLI) specifications from Open Group and ISO/IEC for database APIs and uses Structured Query Language (SQL) as its database access language.  
  
 ODBC is designed for maximum *interoperability* - that is, the ability of a single application to access different database management systems (DBMSs) with the same source code. Database applications call functions in the ODBC interface, which are implemented in database-specific modules called *drivers*. The use of drivers isolates applications from database-specific calls in the same way that printer drivers isolate word processing programs from printer-specific commands. Because drivers are loaded at run time, a user only has to add a new driver to access a new DBMS; it is not necessary to recompile or relink the application.  
  
 This section contains the following topics.  
  
-   [Why Was ODBC Created?](../content/Why-Was-ODBC-Created-.md)  
  
-   [What Is ODBC?](../content/What-Is-ODBC-.md)  
  
-   [ODBC and the Standard CLI](../content/ODBC-and-the-Standard-CLI.md)