---
title: "Descriptors"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ef2cbb93-cd00-40f8-b1d2-5f5723a991aa
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Descriptors
A descriptor handle refers to a data structure that holds information about either columns or dynamic parameters.  
  
 ODBC functions that operate on column and parameter data implicitly set and retrieve descriptor fields. For instance, when **SQLBindCol** is called to bind column data, it sets descriptor fields that completely describe the binding. When **SQLColAttribute** is called to describe column data, it returns data stored in descriptor fields.  
  
 An application calling ODBC functions need not concern itself with descriptors. No database operation requires that the application gain direct access to descriptors. However, for some applications, gaining direct access to descriptors streamlines many operations. For example, direct access to descriptors provides a way to rebind column data, which can be more efficient than calling **SQLBindCol** again.  
  
> [!NOTE]  
>  The physical representation of the descriptor is not defined. Applications gain direct access to a descriptor only by manipulating its fields by calling ODBC functions with the descriptor handle.  
  
 This section contains the following topics.  
  
-   [Types of Descriptors](../content/Types-of-Descriptors.md)  
  
-   [Descriptor Fields](../content/Descriptor-Fields.md)  
  
-   [Allocating and Freeing Descriptors](../content/Allocating-and-Freeing-Descriptors.md)  
  
-   [Getting and Setting Descriptor Fields](../content/Getting-and-Setting-Descriptor-Fields.md)