---
title: "Creating and Terminating Threads"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a2cf98ef-1c71-4742-8ee2-b53fd8e04333
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Creating and Terminating Threads
Multithread applications that use ODBC should call the Microsoft® Visual C++® Run-Time Library functions **_beginthread** and **_endthread** (or **_beginthreadex** and **_endthreadex**) to create and terminate threads that call the ODBC Driver Manager. If applications call the Microsoft Windows NT® functions **CreateThread** and **EndThread** instead, memory leaks will occur because the Driver Manager and some ODBC drivers call C run-time functions that will not work on a thread created by calling **CreateThread**. For more information, see the Microsoft Windows® documentation.