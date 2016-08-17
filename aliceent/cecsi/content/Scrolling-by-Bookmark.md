---
title: "Scrolling by Bookmark"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4862f098-41a4-4bd2-894e-f71bb97f9bc0
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Scrolling by Bookmark
When fetching rows with **SQLFetchScroll**, an application can use a bookmark as a basis for selecting the starting row. This is a form of absolute addressing because it does not depend on the current cursor position. To scroll to a bookmarked row, the application calls **SQLFetchScroll** with a *FetchOrientation* of SQL_FETCH_BOOKMARK. This operation uses the bookmark pointed to by the SQL_ATTR_FETCH_BOOKMARK_PTR statement attribute. It returns the rowset starting with the row identified by that bookmark. An application can specify an offset for this operation in the *FetchOffset* argument of the call to **SQLFetchScroll**. When an offset is specified, the first row of the returned rowset is determined by adding the number in the *FetchOffset* argument to the number of the row identified by the bookmark. This use of the *FetchOffset* argument is not supported when used with ODBC 2.*x* drivers; when an application calls **SQLFetchScroll** in an ODBC 2.*x* driver with *FetchOrientation* set to SQL_FETCH_BOOKMARK, the *FetchOffset* argument must be set to 0.