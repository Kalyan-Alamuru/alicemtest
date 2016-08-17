---
title: "Correlation Names"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 76c36c6f-f8e1-4ece-a77b-611dde3bdd8a
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Correlation Names
Correlation names are fully supported, including within the table list. For example, in the following string, E1 is the correlation name for the table named Emp:  
  
```  
SELECT * FROM Emp E1   
WHERE E1.LastName = 'Smith'  
```