---
title: "Jet: Date, Time, and Timestamp Literals"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 37db1ae1-ca4e-4cd8-9b47-7f1a38e7fcad
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Jet: Date, Time, and Timestamp Literals
For maximum interoperability, applications should pass date literals in the ODBC canonical format using escape-clause syntax:  
  
-   For date literals, {d '*value*'}, where *valu*e is in the form "yyyy-mm-dd"  
  
-   For time literals, {t '*value*'}, where *valu*e is in the form "hh:mm:ss"  
  
 For timestamp literals {ts '*value*'}, where *valu*e is in the form "yyyy-mm-dd hh:mm:ss[.f...]".