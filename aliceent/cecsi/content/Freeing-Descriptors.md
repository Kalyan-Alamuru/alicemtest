---
title: "Freeing Descriptors"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 317213f4-0ebb-4bf8-a37a-4d6b1313823f
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Freeing Descriptors
Explicitly allocated descriptors can be freed either explicitly, by calling **SQLFreeHandle** with *HandleType* of SQL_HANDLE_DESC, or implicitly, when the connection handle is freed. When an explicitly allocated descriptor is freed, all statement handles to which the freed descriptor applied automatically revert to the descriptors implicitly allocated for them.  
  
 Implicitly allocated descriptors can be freed only by calling **SQLDisconnect**, which drops any statements or descriptors open on the connection, or by calling **SQLFreeHandle** with a *HandleType* of SQL_HANDLE_STMT to free a statement handle and all the implicitly allocated descriptors associated with the statement. An implicitly allocated descriptor cannot be freed by calling **SQLFreeHandle** with a *HandleType* of SQL_HANDLE_DESC.  
  
 Even when freed, an implicitly allocated descriptor remains valid, and **SQLGetDescField** can be called on its fields.