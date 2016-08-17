---
title: "ODBC Visual FoxPro Setup Dialog Box"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: de020197-7f53-4643-9cbf-b7887ba88de9
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# ODBC Visual FoxPro Setup Dialog Box
The **ODBC Visual FoxPro Setup** dialog box enables you to add or change a Visual FoxPro data source.  
  
 To download the driver, see [the Visual FoxPro ODBC Driver download site](http://go.microsoft.com/fwlink/?LinkId=121318).  
  
## Dialog Box Options  
 **Data Source Name**  
 Type the name you want to use for the data source.  
  
 **Description**  
 Type a description for the data source.  
  
 **Database type**  
 Lets you choose the type of database you want your data source to connect to.  
  
 **Visual FoxPro database (.DBC)**  
 Specifies that the data source connects to a Visual FoxPro [database](../content/Visual-FoxPro-Terminology.md) (.dbc file) and to all the tables and local views in the database.  
  
 **Free Table directory**  
 Specifies that the data source connects to a directory of [free tables](../content/Visual-FoxPro-Terminology.md). Any [database](../content/Visual-FoxPro-Terminology.md) tables in the same directory are ignored by ODBC catalog functions such as [SQLColumns](../content/SQLColumns--Visual-FoxPro-ODBC-Driver-.md) or [SQLTables](../content/SQLTables--Visual-FoxPro-ODBC-Driver-.md). Database tables can be accessed by using SQL SELECT statements sent through [SQLExecute](../content/SQLExecute--Visual-FoxPro-ODBC-Driver-.md) and [SQLExecDirect](../content/SQLExecDirect--Visual-FoxPro-ODBC-Driver-.md).  
  
 **Path**  
 Displays the path and name for the database or the directory of free tables to which the data source connects.  
  
 **Browse**  
 Enables you to search your system and network for the database or directory to which you want to connect the data source.  
  
 **Options**  
 Expands the dialog box so that you can set Visual FoxPro ODBC Driver options.  
  
## Driver  
 **Collating sequence**  
 The sequence in which fields are sorted. The default sequences reflect the sequences supported by your language version of the operating system. For a list of supported collating sequences, see [SET COLLATE](../content/SET-COLLATE-Command.md).  
  
 **Exclusive**  
 When this check box is selected, the driver opens the Visual FoxPro database exclusively when you access data using the data source. Other users cannot access the database or the tables in the database while the database is opened exclusively. Tables within the exclusively opened database are opened as SHARED. To open a table exclusively, use the [SET EXCLUSIVE](../content/SET-EXCLUSIVE-Command.md) command. This check box is disabled when **Database type** is set to **Free Table directory**.  
  
 **Null**  
 Determines whether columns created with ALTER TABLE and CREATE TABLE allow null values. If you set Null ON, INSERT – SQL inserts a null value into any column not included in an INSERT – SQL... VALUE clause. A blank is inserted if Null is OFF. You can also control this option through a passed connection string as in the following code:  
  
```  
strCon = "DRIVER=MICROSOFT VISUAL FOXPRO DRIVER;  
SOURCETYPE=DBC;SOURCEDB=D:\Testdata.dbc;BACKGROUNDFETCH=NO;NULL=NO"  
```  
  
 **Deleted**  
 Determines whether rows marked as deleted are returned. You can also control this option through a passed connection string as in the following code:  
  
```  
strCon = "DRIVER=MICROSOFT VISUAL FOXPRO DRIVER;  
SOURCETYPE=DBC;SOURCEDB=D:\Testdata.dbc;BACKGROUNDFETCH=NO;  
DELETED=YES"  
```  
  
 **Fetch data in background**  
 Determines whether records will be fetched in the background (progressive fetching) or your application will wait until all records in the result set are fetched.