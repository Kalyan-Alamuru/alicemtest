---
title: "Bookmarks (ODBC)"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1d7cccc5-f847-4321-b240-28570854ee5c
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Bookmarks (ODBC)
A bookmark is a value used to identify a row of data. The meaning of the bookmark value is known only to the driver or data source. For example, it might be as simple as a row number or as complex as a disk address. Bookmarks in ODBC are a bit different from bookmarks in real books. In a real book, the reader places a bookmark at a specific page and then looks for that bookmark to return to the page. In ODBC, the application requests a bookmark for a particular row, stores it, and passes it back to the cursor to return to the row. Thus, bookmarks in ODBC are similar to a reader writing down a page number, remembering it, and then looking up the page again.  
  
 To determine a driver's support of bookmarks, an application calls **SQLGetInfo** with the SQL_BOOKMARK_PERSISTENCE option. The bits in this value describe what operations bookmarks survive, such as whether bookmarks are still valid after the cursor is closed.  
  
 This section contains the following topics.  
  
-   [Bookmark Types](../content/Bookmark-Types.md)  
  
-   [Retrieving Bookmarks](../content/Retrieving-Bookmarks.md)  
  
-   [Scrolling by Bookmark](../content/Scrolling-by-Bookmark.md)  
  
-   [Updating, Deleting, or Fetching by Bookmark](../content/Updating--Deleting--or-Fetching-by-Bookmark.md)  
  
-   [Comparing Bookmarks](../content/Comparing-Bookmarks.md)