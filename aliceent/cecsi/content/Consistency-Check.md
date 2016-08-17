---
title: "Consistency Check"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: deb80efa-ad1f-4ea5-b334-9817cd279e5c
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Consistency Check
A consistency check is performed by the driver automatically whenever an application sets the SQL_DESC_DATA_PTR field of the APD, ARD, or IPD. Whenever this field is set, the driver checks that the value of the SQL_DESC_TYPE field and the values applicable to the SQL_DESC_TYPE field in the same record are valid and consistent.  
  
 The SQL_DESC_DATA_PTR field of an IPD is not normally set; however, an application can do so to force a consistency check of IPD fields. The value that the SQL_DESC_DATA_PTR field of the IPD is set to is not actually stored and cannot be retrieved by a call to **SQLGetDescField** or **SQLGetDescRec**; the setting is made only to force the consistency check. A consistency check cannot be performed on an IRD.  
  
 For more information on the consistency check, see [SQLSetDescRec](../content/SQLSetDescRec-Function.md).