---
title: "Supported Data Types"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a89d4bab-ef3c-45c2-aa72-2639b3e0f856
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Supported Data Types
The data types supported by DBMSs vary considerably. An application can determine the names and characteristics of supported data types by calling **SQLGetTypeInfo**. Because of wide variation in data type names, the application must use the data type names returned by **SQLGetTypeInfo** in **CREATE TABLE** statements. For more information, see [Data Types in ODBC](../content/Data-Types-in-ODBC.md).