---
title: "CREATE INDEX Statement"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 69438247-eef3-44c5-bef2-acef4e146f41
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# CREATE INDEX Statement
The syntax of the CREATE INDEX statement is:  
  
 CREATE [UNIQUE] INDEX *index-name* ON *table-name* (*column-identifier* [ASC][DESC][, *column-identifier* [ASC][DESC]...]) WITH <*index option list*>  
  
 where <*index option list*> can be: PRIMARY &#124; DISALLOW NULL &#124; IGNORE NULL  
  
 Only the Microsoft Access driver uses the DISALLOW NULL and IGNORE NULL index options. The dBASE and Paradox drivers accept the syntax, but ignore the presence of either option.  
  
 When the Paradox driver is used, the CREATE INDEX statement creates Paradox primary key files and secondary files.  
  
 This statement is not supported by the Microsoft Excel or Text drivers.