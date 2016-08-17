---
title: "Generic Applications"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dda2a3c4-76ef-40a6-b3a1-9e95bed61618
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Generic Applications
Generic applications sometimes perform a hard-coded task, such as a spreadsheet retrieving data from a database. They might also perform a variety of user-defined tasks, such as a generic query application allowing the user to enter and execute an SQL statement. What generic applications have in common is that they must work with a variety of different DBMSs and that the developer does not know beforehand what these DBMSs will be.  
  
 Therefore, generic applications need to be highly interoperable. The developer must make many choices, trading off interoperability for features, and must write code that expects drivers to support a wide range of functionality. While generic applications might be tuned to work with popular DBMSs, they rarely contain driver-specific or DBMS-specific code.