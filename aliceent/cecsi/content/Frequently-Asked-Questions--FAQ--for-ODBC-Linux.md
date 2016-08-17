---
title: "Frequently Asked Questions (FAQ) for ODBC Linux"
ms.custom: na
ms.date: 07/18/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 65bfd6d2-c83d-4528-a5e1-a85b125a4f4a
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pt-br
  - ru-ru
  - zh-cn
  - zh-tw
---
# Frequently Asked Questions (FAQ) for ODBC Linux
The following are answers to questions about the ODBC Driver for  SQL Server  on Linux.  
  
## Frequently Asked Questions  
How do existing ODBC applications on Linux work with the driver?  
You should be able to compile and run the ODBC applications that you have been compiling and running on Linux using other drivers.  
  
Which features of  SQL Server 2012  does this version of the driver support?  
The ODBC driver on Linux supports all server features in  SQL Server 2012  except LocalDB. For more information about  SQL Server  supported features, see [Programming Guidelines](../content/Programming-Guidelines.md).  
  
Does the driver support Kerberos authentication?  
Yes, for more information, see [Using Integrated Authentication](../content/Using-Integrated-Authentication.md).  
  
Which Unicode encoding should an application use?  
UTF-8 for SQL_CHAR data and UTF-16 for SQL_WCHAR data.  
  
Are there ODBC samples that I can download and run with the driver to experiment with it or evaluate it?  
See [Use Existing MSDN C++ ODBC Samples for the ODBC Driver on Linux](http://blogs.msdn.com/b/sqlblog/archive/2012/01/26/use-existing-msdn-c-odbc-samples-for-microsoft-linux-odbc-driver.aspx) for a sample.  
  
Is the ODBC driver on Linux open source?  
No, the ODBC driver on Linux is not an open source product.  
  
Why must users build the UnixODBC Driver Manager?  
The UnixODBC Driver Manager package that ships with most Linux distributions is not compatible with this release of the  Microsoft  ODBC Driver for  SQL Server . For information on how to install version 2.3.0 or 2.3.1 of the unixODBC Driver Manager, see [Installing the Driver Manager](../content/Installing-the-Driver-Manager.md).  
  
What are the differences between the  Microsoft  SQL Server  ODBC Driver 1.0 for Linux and the  Microsoft  ODBC Driver 13 (Preview) or 11 for  SQL Server ? Are they the same product?  
The  Microsoft  ODBC Driver 11 for  SQL Server  is the new name for the driver for Linux and Windows. If you are using the  Microsoft  SQL Server  ODBC Driver 1.0 for Linux, you should upgrade to the  Microsoft  ODBC Driver 13 (Preview) or 11 for  SQL Server .  
  
