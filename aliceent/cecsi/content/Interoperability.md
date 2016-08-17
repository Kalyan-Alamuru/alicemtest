---
title: "Interoperability"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 43b7c849-9d59-4002-9977-9e2c8730b859
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Interoperability
*Interoperability* is the ability of a single application to operate with many different DBMSs. The need to write generic, interoperable applications was one of the major factors leading to the development of ODBC. However, interoperability is not a simple path followed from "not interoperable" to "completely interoperable." The path has many branches, and each requires trade-offs among features, speed, code complexity, and development time.  
  
 The process of writing an interoperable application follows several steps:  
  
1.  Deciding whether the application will use ODBC.  
  
2.  Choosing a level of interoperability and deciding which trade-offs are necessary to reach that level.  
  
3.  Writing interoperable code and testing it as fully as possible.  
  
 It should be noted that interoperability is primarily the domain of the application writer. Drivers are designed to work with a single DBMS and, by definition, are not interoperable. They play a role in interoperability by correctly implementing and exposing ODBC over a single DBMS.  
  
 This section contains the following topics.  
  
-   [Is ODBC the Answer?](../content/Is-ODBC-the-Answer-.md)  
  
-   [Choosing a Level of Interoperability](../content/Choosing-a-Level-of-Interoperability.md)  
  
-   [Determining the Target DBMSs and Drivers](../content/Determining-the-Target-DBMSs-and-Drivers.md)  
  
-   [Considering Database Features to Use](../content/Considering-Database-Features-to-Use.md)  
  
-   [Length of the Product Cycle](../content/Length-of-the-Product-Cycle.md)  
  
-   [Writing an Interoperable Application](../content/Writing-an-Interoperable-Application.md)  
  
-   [Testing Interoperable Applications](../content/Testing-Interoperable-Applications.md)