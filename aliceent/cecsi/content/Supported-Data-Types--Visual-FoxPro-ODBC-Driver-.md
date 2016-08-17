---
title: "Supported Data Types (Visual FoxPro ODBC Driver)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ab529cc6-d157-4b35-b6f9-6ffd09af098c
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Supported Data Types (Visual FoxPro ODBC Driver)
The list of data types supported by the driver are presented through the ODBC API and in Microsoft Query.  
  
## Data Types in C Applications  
 You can obtain a list of data types supported by the Visual FoxPro ODBC Driver by using the [SQLGetTypeInfo](../content/SQLGetTypeInfo--Visual-FoxPro-ODBC-Driver-.md) function in C or C++ applications.  
  
## Data Types in Applications Using Microsoft Query  
 If your application uses Microsoft Query to create a new table on a Visual FoxPro data source, Microsoft Query displays the **New Table Definition** dialog box. Under **Field Description**, the **Type** box lists [Visual FoxPro field data types](../content/Visual-FoxPro-Field-Data-Types.md), represented by single characters.