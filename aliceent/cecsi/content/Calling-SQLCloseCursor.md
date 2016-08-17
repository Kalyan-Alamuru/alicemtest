---
title: "Calling SQLCloseCursor"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ef448c39-a9ad-4f07-8ef3-65bd4cef672a
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Calling SQLCloseCursor
Because **SQLCloseCursor** is almost the same as **SQLFreeStmt** with SQL_CLOSE, the Driver Manager does not map this function. Replacement functions are mapped so that existing ODBC 2*.x* applications can easily move to ODBC 3.*x* by using the new functions. Such a move makes it easier for such applications to begin using new ODBC 3.*x* functionality inside of conditional code in a modular fashion. **SQLCloseCursor** does not represent any new functionality. An application does not gain any advantage by moving to **SQLCloseCursor** from **SQLFreeStmt** with SQL_CLOSE.