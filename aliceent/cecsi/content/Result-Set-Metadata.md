---
title: "Result Set Metadata"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6d134515-e34d-4563-96d7-8ad7714818fd
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Result Set Metadata
*Metadata* is data that describes other data. For example, result set metadata describes the result set, such as the number of columns in the result set, the data types of those columns, their names, precision, nullability, and so on.  
  
 Interoperable applications should always check the metadata of result set columns. The metadata for a column in a result set might differ from the metadata for the column as returned by a catalog function. For example, suppose that an updatable column is included in a result set created by joining two tables. While **SQLColumnPrivileges** might indicate that a user can update the column, the result set metadata might not if the column is on the "many" side of the join; many data sources can update columns on the "one" side of a join but not on the "many" side. Even data types cannot be assumed to be the same, because the data source might promote the data type while creating the result set.  
  
 This section contains the following topics.  
  
-   [How is Metadata Used?](../content/How-is-Metadata-Used-.md)  
  
-   [SQLDescribeCol and SQLColAttribute](../content/SQLDescribeCol-and-SQLColAttribute.md)