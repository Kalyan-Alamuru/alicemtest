---
title: "View a Job"
ms.custom: na
ms.date: 08/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d2241a3f-dbcf-433c-b7bc-f96bdf0eac8c
caps.latest.revision: 4
caps.handback.revision: 0
manager: jhubbard
translation.priority.mt: 
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
# View a Job
This topic describes how to view  Microsoft   SQL Server  Agent jobs in SQL Server 2016 by using SQL Server Management Studio or  Transact\-SQL .  
  
**In This Topic**  
  
-   **Before you begin:**  
  
    [Security](#Security)  
  
-   **To view a job, using:**  
  
    [SQL Server Management Studio](#SSMS)  
  
    [Transact-SQL](#TSQL)  
  
    [SQL Server Management Objects](#SMO)  
  
## <a name="BeforeYouBegin"></a>Before You Begin  
  
### <a name="Security"></a>Security  
You can only view jobs that you own, unless you are a member of the **sysadmin** fixed server role. Members of this role can view all jobs. For detailed information, see [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMS"></a>Using SQL Server Management Studio  
  
#### To view a job  
  
1.  In **Object Explorer,** connect to an instance of the SQL Server Database Engine, and then expand that instance.  
  
2.  Expand **SQL Server Agent**, and then expand **Jobs**.  
  
3.  Right-click a job, and then click **Properties**.  
  
## <a name="TSQL"></a>Using Transact-SQL  
  
#### To view a job  
  
1.  In **Object Explorer**, connect to an instance of  Database Engine .  
  
2.  On the Standard bar, click **New Query**.  
  
3.  Copy and paste the following example into the query window and click **Execute**.  
  
    ```  
    -- lists all aspects of the information for the job NightlyBackups.  
    USE msdb ;  
    GO  
  
    EXEC dbo.sp_help_job  
        @job_name = N'NightlyBackups',  
        @job_aspect = N'ALL' ;  
    GO  
    ```  
  
## <a name="SMO"></a>Using SQL Server Management Objects  
**To view a job**  
  
Use the **Job** class by using a programming language that you choose, such as Visual Basic, Visual C#, or PowerShell. For more information, see [SQL Server Management Objects (SMO)](http://msdn.microsoft.com/library/ms162169.aspx).  
  
