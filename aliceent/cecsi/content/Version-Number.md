---
title: "Version Number"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6eccacdf-b837-4b66-bd48-ba31771acecb
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Version Number
There are several versions of ODBC, each with different features. An application determines which ODBC version the Driver Manager and a particular driver support by calling **SQLGetInfo** with the SQL_ODBC_VER and SQL_DRIVER_ODBC_VER options.