---
title: "Download SQL Server Management Studio (SSMS)"
ms.custom: na
ms.date: 2016-08-15
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: adafeeef-4255-4924-8042-02f503d599ca
caps.latest.revision: 111
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
# Download SQL Server Management Studio (SSMS)
SQL Server Management Studio (SSMS) is an integrated environment for accessing, configuring, managing, administering, and developing all components of SQL Server. SSMS combines a broad group of graphical tools with a number of rich script editors to provide developers and administrators of all skill levels access to SQL Server. This release features improved compatibility with previous versions of SQL Server, a stand-alone web installer, and toast notifications within SSMS when new releases become available.  
     
| ![download](../content/media/download.png) Download SQL Server Management Studio (SSMS)  |  
|---|  
|**[Download SQL Server Management Studio](http://go.microsoft.com/fwlink/?LinkID=824938)**|  

> [!NOTE]  
> * SSMS releases are now branded numerically, not by months.
> * This generally available release of SSMS is free and does not require a SQL Server license to install and use.  



 
## SQL Server Management Studio   
**Version Information**  
  
*This release of SSMS uses the Visual Studio 2015 Isolated shell.*   
The version number for this release: 16
  
**Supported SQL Server versions**  
  
* This version of SSMS works with all [supported versions of SQL Server (SQL Server 2008 - SQL Server 2016),](https://support.microsoft.com/en-us/lifecycle?C2=1044) and provides the greatest level of support for working with the latest cloud features in Azure SQL Database.  
* There is no explicit block for SQL Server 2000 or SQL Server 2005, but some features may not work properly.  
* Additionally, this version of SSMS can be installed side-by-side with earlier released non-preview versions.  
  
**Supported Operating systems**  
  
This release of SSMS supports the following platforms when used with the latest available service pack:   
 Windows 10, Windows 8, Windows 8.1, Windows 7 (SP1), Windows Server 2012 (64-bit), Windows Server 2012 R2 (64-bit), Windows Server 2008 R2 (64-bit)  
   
 **Available Languages**  
> [!NOTE]  
> Non-English localized releases of SSMS require the [KB 2862966 security update package](https://support.microsoft.com/en-us/kb/2862966) if installing on: Windows 8, Windows 7, Windows Server 2012, and Windows Server 2008 R2. 
  
 This release of SSMS can be installed in the following languages:  
[Chinese (People's Republic of China)](http://go.microsoft.com/fwlink/?LinkID=824938&clcid=0x804) | [Chinese (Taiwan)](http://go.microsoft.com/fwlink/?LinkID=824938&clcid=0x404) | [English (United States)](http://go.microsoft.com/fwlink/?LinkID=824938&clcid=0x409) | [French](http://go.microsoft.com/fwlink/?LinkID=824938&clcid=0x40c)  
[German](http://go.microsoft.com/fwlink/?LinkID=824938&clcid=0x407) | [Italian](http://go.microsoft.com/fwlink/?LinkID=824938&clcid=0x410) | [Japanese](http://go.microsoft.com/fwlink/?LinkID=824938&clcid=0x411) | [Korean](http://go.microsoft.com/fwlink/?LinkID=824938&clcid=0x412) | [Portuguese (Brazil)](http://go.microsoft.com/fwlink/?LinkID=824938&clcid=0x416) | [Russian](http://go.microsoft.com/fwlink/?LinkID=824938&clcid=0x419) | [Spanish](http://go.microsoft.com/fwlink/?LinkID=824938&clcid=0x40a)  

 
## Changelog  

* SSMS monthly releases are now branded numerically not by months.

* New authentication option **'Active Directory Universal Authentication'**. This is a token-based authentication mechanism driven by Azure Active Directory that supports multi-factor, password, and integrated authentication mechanisms. [Learn more about Active Directory Universal Authentication.](https://azure.microsoft.com/documentation/articles/sql-database-ssms-mfa-authentication/)

* New Extended Events templates matching the functionality of SQL Server Profiler templates [(Microsoft Connect item #2543925).](https://connect.microsoft.com/SQLServer/feedback/details/2543925/sql-server-extended-events-profiler-tool) Learn more about the included [SQL Server Profiler templates.](https://msdn.microsoft.com/library/ms190176.aspx)

* New 'Get-SqlLogin' and 'Remove-SqlLogin' cmdlets to help perform SQL Server login management using PowerShell [(Microsoft Connect item #2588952).](https://connect.microsoft.com/SQLServer/feedback/details/2588952/)

* New PowerShell cmdlet 'New-SqlColumnMasterKeySettings' that adds support for creation of column master keys for arbitrary providers and key paths.

* New 'Create database' dialog to streamline creation of Azure SQL databases in SSMS.

* Support for filtering in the 'Databases' node of SSMS Object Explorer. Navigate to the 'Databases' node in Object explorer and click the filter icon in the Object explorer toolbar to filter the list of databases.

* Support for Azure-Resource Manager (ARM) type storage accounts in the Backup and Restore wizards.

* [Initial beta support for high-resolution displays](https://blogs.msdn.microsoft.com/sqlreleaseservices/ssms-highdpi-support/)[ (Microsoft Connect item #1129301)](https://connect.microsoft.com/SQLServer/feedback/details/1129301/management-studio-is-unusable-on-a-4k-display).

* Improvements in Database Engine Tuning Advisor (DTA) to support automatically reading a workload from the SQL Server Query Store.

* Improvements in Database Engine Tuning Advisor (DTA) to display index recommendations for clustered columnstore indexes, non-clustered columnstore indexes, and rowstore indexes.

* Support for sending Database Console (DBCC) commands using SQL Server Analysis Services PowerShell cmdlets.

* Bug fix to view cleartext of decrypted AlwaysEncrypted large object (LOB) columns in SSMS [(Microsoft Connect item #2413024).](https://connect.microsoft.com/SQLServer/feedback/details/2413024/cannot-view-cleartext-of-alwaysencrypted-lob-columns-in-ssms)

* Bug fix in Always Encrypted dialog to fix crash when Windows visual styles are not enabled (e.g. enabling high contrast display).

* Bug fix for 'Method not found' error preventing connection to SQL Server instances.

* Bug fix for SSMS crash when creating a partition function with datetime offset.

* Bug fix to remove Microsoft .NET 3.5 requirement for starting Distributed Replay administration tool (DReplay.exe).

* Bug fix in Analysis Services Deployment wizard to support fully-qualified server names.

* Bug fix in SSMS to display partitions in Analysis Services tabular models with a 2016 compatibility model [(Microsoft Connect item #2845053).](https://connect.microsoft.com/SQLServer/feedback/details/2845053/ssms-cannot-display-partitions-in-tabular-models-in-2016-compatibility-level) 

* Performance improvements and bug fixes in Analysis services tabular models, and SQL Server Shared Management Objects (SMO). 

For the full list of features, see   
                [SQL Server Management Studio - Changelog (SSMS)](../content/SQL-Server-Management-Studio---Changelog--SSMS-.md)  
  
To see the list of known issues and work arounds, see   
                [SQL Server Management Studio -  Release Notes](../content/SQL-Server-Management-Studio----Release-Notes.md)  
  
For information about user data collection, see   
                [SQL Server Privacy Statement](http://www.microsoft.com/privacystatement/en-us/SQLServer/Default.aspx).  
  
## Previous releases  
[Previous SQL Server Management Studio Releases](../content/Previous-SQL-Server-Management-Studio-Releases.md)  
  
## Feedback  
  
![needhelp_person_icon](../content/media/needhelp_person_icon.png) [SQL Client Tools Forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=sqltools) |  [Log an issue or suggestion at Microsoft Connect](https://connect.microsoft.com/SQLServer/Feedback).  
  
## See Also  
[Tutorial: SQL Server Management Studio](assetId:///d2bade70-07cf-4d94-b5d2-88aecb538ed1)  
[SQL Server Management Studio documentation](https://msdn.microsoft.com/library/hh213248(v=sql.130).aspx)  
[Microsoft SQL Server](https://msdn.microsoft.com/library/bb545450.aspx)  
[Additional updates and service packs](https://technet.microsoft.com/sqlserver/ff803383.aspx)  
[Download SQL Server Data Tools (SSDT)](../content/Download-SQL-Server-Data-Tools--SSDT-.md)  
