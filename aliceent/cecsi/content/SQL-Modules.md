---
title: "SQL Modules"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 07551472-87ee-4765-951f-1364ed32f0c0
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQL Modules
The second technique for sending SQL statements to the DBMS is through modules. Briefly, a module consists of a group of procedures, which are called from the host programming language. Each procedure contains a single SQL statement, and data is passed to and from the procedure through parameters.  
  
 A module can be thought of as an object library that is linked to the application code. However, exactly how the procedures and the rest of the application are linked is implementation-dependent. For example, the procedures could be compiled into object code and linked directly to the application code, they could be compiled and stored on the DBMS and calls to access plan identifiers placed in the application code, or they could be interpreted at run time.  
  
 The main advantage of modules is that they cleanly separate SQL statements from the programming language. In theory, it should be possible to change one without changing the other and simply relink them.