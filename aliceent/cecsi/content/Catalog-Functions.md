---
title: "Catalog Functions"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 81ba9453-c085-47c0-b411-90ca6a5ee428
caps.latest.revision: 7
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Catalog Functions
All databases have a structure that outlines how data will be stored in the database. For example, a simple sales order database might have the structure shown in the following illustration, in which the ID columns are used to link the tables.  
  
 ![Shows the structure of a simple database](../content/media/pr19.gif "pr19")  
  
 This structure, along with other information such as privileges, is stored in a set of system tables called the database's *catalog,* which is also known as a *data dictionary*.  
  
 An application can discover this structure through calls to the *catalog functions*. The catalog functions return information in result sets and are usually implemented through **SELECT** statements against the tables in the catalog. For example, an application might request a result set containing information about all the tables on the system or all the columns in a particular table.  
  
 This section contains the following topics.  
  
-   [Uses of Catalog Data](../content/Uses-of-Catalog-Data.md)  
  
-   [Catalog Functions in ODBC](../content/Catalog-Functions-in-ODBC.md)