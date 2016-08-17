---
title: "How is Metadata Used?"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 70fb976c-9342-4edd-b066-1140696fd0fa
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# How is Metadata Used?
Applications require metadata for most result set operations. For example, the application uses the data type of a column to determine what kind of variable to bind to that column. It uses the byte length of a character column to determine how much space it needs to display data from that column. How an application determines the metadata for a column depends on the type of the application.  
  
 Vertical applications work with predefined tables and perform predefined operations on those tables. Because the result set metadata for such applications is defined before the application is even written and is controlled by the application developer, it can be hard-coded into the application. For example, if an order ID column is defined as a 4-byte integer in the data source, the application can always bind a 4-byte integer to that column. When metadata is hard-coded in the application, a change to the tables used by the application generally implies a change to the application code. This is rarely a problem, because such changes are usually made as part of a new release of the application.  
  
 Like vertical applications, custom applications generally work with predefined tables and perform predefined operations on those tables. For example, an application might be written to transfer data among three different data sources; the data to be transferred is usually known when the application is written. Thus, custom applications also tend to have hard-coded metadata.  
  
 Generic applications, especially those that support ad hoc queries, almost never know the metadata of the result sets they create. Therefore, they must discover the metadata at run time using the functions **SQLNumResultCols**, **SQLDescribeCol**, and **SQLColAttribute**, which are described in the next section, [SQLDescribeCol and SQLColAttribute](../content/SQLDescribeCol-and-SQLColAttribute.md).  
  
 All applications, regardless of their type, can hard-code metadata for the result sets returned by the catalog functions. These result sets are defined in the reference section of this manual.