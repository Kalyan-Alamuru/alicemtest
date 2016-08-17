---
title: "Managing Data Sources"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 67cc4945-4850-4eb4-8da6-b835ddaeca4c
caps.latest.revision: 11
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Managing Data Sources
After you have installed an ODBC driver from the driver's setup program, you can define one or more data sources for it. The data source name (DSN) should provide a unique description of the data; for example, *Payroll* or *Accounts Payable*. The user and system data sources that are defined for all currently installed drivers are listed in the **User DSN** or **System DSN** tabs of the **ODBC Data Source Administrator** dialog box. The file data sources in a given directory are listed in the **File DSN** tab; the directory to be shown is entered in the **Look in** box in the **File DSN** tab.  
  
> [!NOTE]  
>  To manage a data source that connects to a 32-bit driver under 64-bit platform, use c:\windows\sysWOW64\odbcad32.exe. To manage a data source that connects to a 64-bit driver, use c:\windows\system32\odbcad32.exe. In **Administrative Tools** on a 64-bit Windows 8 operating system, there are icons for both the 32-bit and 64-bit **ODBC Data Source Administrator** dialog box.  
  
 If you use the 64-bit odbcad32.exe to configure or remove a DSN that connects to a 32-bit driver, for example, **Driver do Microsoft Access (\*.mdb)**, you will receive the following error message:  
  
```  
The specified DSN contains an architecture mismatch between the Driver and Application  
```  
  
 To resolve this error, use the 32-bit odbcad32.exe to configure or remove the DSN.  
  
 A data source associates a particular ODBC driver with the data you want to access through that driver. For example, you might create a data source to use the ODBC dBASE driver to access one or more dBASE files found in a specific directory on your hard disk or a network drive. Using the ODBC Data Source Administrator, you can add, modify, and delete data sources, as described in the following table.  
  
|Action|Description|  
|------------|-----------------|  
|Adding data sources|It is possible to add multiple data sources, each one associating a driver with some data you want to access by using that driver. Give each data source a name that uniquely identifies that data source. For example, if you create a data source for a set of dBASE files that contain customer information, you might name the data source "Customers." Applications typically display data source names for users to choose from.<br /><br /> Adding a file data source is slightly different from adding user or system data sources. For more information, see the ODBC Data Source Administrator help file.|  
|Modifying data sources|Depending on your requirements, you might find it necessary to reconfigure data sources. You can reset options by clicking **Configure** in any driver setup dialog box.|  
|Deleting data sources|Click **Remove** after selecting a data source.|  
  
 For more information about file data sources, see [Connecting Using File Data Sources](../content/Connecting-Using-File-Data-Sources.md) or the [SQLDriverConnect Function](../content/SQLDriverConnect-Function.md).  
  
## See Also  
 [ODBC Data Source Administrator](../content/ODBC-Data-Source-Administrator.md)