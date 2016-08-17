---
title: "SQL_NO_DATA"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 07a4144a-a548-4578-b2be-715c3cf73bf8
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQL_NO_DATA
When an ODBC 3.*x* application calls **SQLExecDirect**, **SQLExecute**, or **SQLParamData** in an ODBC 2.*x* driver to execute a searched update or delete statement that does not affect any rows at the data source, the driver should return SQL_SUCCESS, not SQL_NO_DATA. When an ODBC 2.*x* or ODBC 3.*x* application working with an ODBC 3.*x* driver calls **SQLExecDirect**, **SQLExecute**, or **SQLParamData** with the same result, the ODBC 3.*x* driver should return SQL_NO_DATA.