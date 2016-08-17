---
title: "Static SQL"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 667d92ec-fed9-4028-81d4-bb9ba867356a
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Static SQL
The embedded SQL shown in [Embedded SQL Example](../content/Embedded-SQL-Example.md) is known as static SQL. It is called static SQL because the SQL statements in the program are static; that is, they do not change each time the program is run. As described in the previous section, these statements are compiled when the rest of the program is compiled.  
  
 Static SQL works well in many situations and can be used in any application for which the data access can be determined at program design time. For example, an order-entry program always uses the same statement to insert a new order, and an airline reservation system always uses the same statement to change the status of a seat from available to reserved. Each of these statements would be generalized through the use of host variables; different values can be inserted in a sales order, and different seats can be reserved. Because such statements can be hard-coded in the program, such programs have the advantage that the statements need to be parsed, validated, and optimized only once, at compile time. This results in relatively fast code.