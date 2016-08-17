---
title: "Visual FoxPro Field Data Types"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 50b733dc-679a-4b10-bc5d-98bb474dead2
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Visual FoxPro Field Data Types
The following table lists the values for the *FieldType* argument in ALTER TABLE and CREATE TABLE and indicates whether *nFieldWidth* and *nPrecision* arguments are required.  
  
|*FieldType*|*NFieldWidth*|*nPrecision*|Description|  
|-----------------|-------------------|------------------|-----------------|  
|B|-|d|Double|  
|C|N|-|Character field of width *n*|  
|D|-|-|Date|  
|F|N|d|Floating numeric field of width *n* with *d* decimal places|  
|G|-|-|General|  
|I|-|-|Integer|  
|L|-|-|Logical|  
|M|-|-|Memo|  
|N|N|d|Numeric field of width *n* with *d* decimal places|  
|T|-|-|DateTime|  
|Y|-|-|Currency|