---
title: "Binding Columns for Use with Block Cursors"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 231beede-cdfa-4e28-8b10-2760b983250f
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Binding Columns for Use with Block Cursors
Because block cursors return multiple rows, applications that use them must bind an array of variables to each column instead of a single variable. These arrays are collectively known as the *rowset buffers*. Following are the two styles of binding:  
  
-   Bind an array to each column. This is called *column-wise binding* because each data structure (array) contains data for a single column.  
  
-   Define a structure to hold the data for an entire row and bind an array of these structures. This is called *row-wise binding* because each data structure contains the data for a single row.  
  
 As when the application binds single variables to columns, it calls **SQLBindCol** to bind arrays to columns. The only difference is that the addresses passed are array addresses, not single variable addresses. The application sets the SQL_BIND_BY_COLUMN statement attribute to specify whether it is using column-wise or row-wise binding. Whether to use column-wise or row-wise binding is largely a matter of application preference. Row-wise binding might correspond more closely to the application's layout of data, in which case it would provide better performance.  
  
 This section contains the following topics.  
  
-   [Column-Wise Binding](../content/Column-Wise-Binding.md)  
  
-   [Row-Wise Binding](../content/Row-Wise-Binding.md)