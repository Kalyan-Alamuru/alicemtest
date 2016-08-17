---
title: "Comparing Bookmarks"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ea347635-fbe3-41c1-b537-4048b7c0f7da
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Comparing Bookmarks
Because bookmarks are byte-comparable, they can be compared for equality or inequality. To do so, an application treats each bookmark as an array of bytes and compares two bookmarks byte-by-byte. Because bookmarks are guaranteed to be distinct only within a result set, it makes no sense to compare bookmarks that were obtained from different result sets.