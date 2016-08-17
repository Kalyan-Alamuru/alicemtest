---
title: "File Data Sources"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: db245c80-981a-4638-bd03-69d04bc67af0
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# File Data Sources
*File data sources* are stored in a file and allow connection information to be used repeatedly by a single user or shared among several users. When a file data source is used, the Driver Manager makes the connection to the data source using the information in a .dsn file. This file can be manipulated like any other file. A file data source does not have a data source name, as does a machine data source, and is not registered to any one user or machine.  
  
 A file data source streamlines the connection process, because the .dsn file contains the connection string that would otherwise have to be built for a call to the **SQLDriverConnect** function. Another advantage of the .dsn file is that it can be copied to any machine, so identical data sources can be used by many machines as long as they have the appropriate driver installed. A file data source can also be shared by applications. A shareable file data source can be placed on a network and used simultaneously by multiple applications.  
  
 A .dsn file can also be unshareable. An unshareable .dsn file resides on a single machine and points to a machine data source. Unshareable file data sources exist mainly to allow the easy conversion of machine data sources to file data sources so that an application can be designed to work solely with file data sources. When the Driver Manager is sent the information in an unshareable file data source, it connects as necessary to the machine data source that the .dsn file points to.  
  
 For more information about file data sources, see [Connecting Using File Data Sources](../content/Connecting-Using-File-Data-Sources.md), or the [SQLDriverConnect](../content/SQLDriverConnect-Function.md) function description.