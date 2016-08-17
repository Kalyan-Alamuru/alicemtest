---
title: "Data Sources"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4ae44fa2-0b9b-4e19-ab45-c1dc93b68406
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Data Sources
A *data source* is simply the source of the data. It can be a file, a particular database on a DBMS, or even a live data feed. The data might be located on the same computer as the program, or on another computer somewhere on a network. For example, a data source might be an Oracle DBMS running on an OS/2® operating system, accessed by Novell® Netware; an IBM DB2 DBMS accessed through a gateway; a collection of Xbase files in a server directory; or a local Microsoft® Access database file.  
  
 The purpose of a data source is to gather all of the technical information needed to access the data — the driver name, network address, network software, and so on — into a single place and hide it from the user. The user should be able to look at a list that includes Payroll, Inventory, and Personnel, choose Payroll from the list, and have the application connect to the payroll data, all without knowing where the payroll data resides or how the application got to it.  
  
 The term *data source* should not be confused with similar terms. In this manual, *DBMS* or *database* refers to a database program or engine. A further distinction is made between *desktop databases,* designed to run on personal computers and often lacking in full SQL and transaction support, and *server databases,* designed to run in a client/server situation and characterized by a stand-alone database engine and rich SQL and transaction support. *Database* also refers to a particular collection of data, such as a collection of Xbase files in a directory or a database on SQL Server. It is generally equivalent to the term *catalog,* used elsewhere in this manual, or the term *qualifier* in earlier versions of ODBC.  
  
 This section contains the following topics.  
  
-   [Types of Data Sources](../content/Types-of-Data-Sources.md)  
  
-   [Using Data Sources](../content/Using-Data-Sources.md)  
  
-   [Data Source Example](../content/Data-Source-Example.md)