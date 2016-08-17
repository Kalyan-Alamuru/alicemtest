---
title: "Calling SQLGetDiagField"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3c4fb606-b81c-4f11-9820-f0a54e3bc401
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Calling SQLGetDiagField
When an ODBC 3.*x* application calls **SQLGetDiagField** in an ODBC 2*.x* driver, the driver will return SQL_SUCCESS and the appropriate information in *\*DiagInfoPtr* if the *DiagIdentifier* argument is SQL_DIAG_CLASS_ORIGIN, SQL_DIAG_CLASS_SUBCLASS_ORIGIN, SQL_DIAG_CONNECTION_NAME, SQL_DIAG_MESSAGE_TEXT, SQL_DIAG_NATIVE, SQL_DIAG_NUMBER, SQL_DIAG_RETURNCODE, SQL_DIAG_SERVER_NAME, or SQL_DIAG_SQLSTATE. All other diagnostic fields will return SQL_ERROR.