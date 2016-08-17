---
title: "Modify the Target Servers for a Job"
ms.custom: na
ms.date: 08/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9dbe24f2-acec-4aa2-920c-e8e96efa18e4
caps.latest.revision: 5
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
# Modify the Target Servers for a Job
This topic describes how to change the target servers for  Microsoft   SQL Server  Agent jobs in SQL Server 2016 by using SQL Server Management Studio or  Transact\-SQL .  
  
**In This Topic**  
  
-   **Before you begin:**  
  
    [Security](#Security)  
  
-   **To modify the target servers for a job, using:**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
## <a name="BeforeYouBegin"></a>Before You Begin  
  
### <a name="Security"></a>Security  
  
#### <a name="Permissions"></a>Permissions  
By default, members of the sysadmin fixed server role can execute this stored procedure. Other users must be granted one of the following SQL Server Agent fixed database roles in the msdb database:  
  
1.  **SQLAgentUserRole**  
  
2.  **SQLAgentReaderRole**  
  
3.  SQLAgentOperatorRole  
  
## <a name="SSMSProcedure"></a>Using SQL Server Management Studio  
  
#### To modify the target servers for a job  
  
1.  In **Object Explorer,** connect to an instance of the SQL Server Database Engine, and then expand that instance.  
  
2.  Expand **SQL Server Agent**, expand **Jobs**, right-click a job, and then click **Properties**.  
  
3.  In the **Job Properties** dialog, select the **Targets**page, and click **Target local server**, or **Target multiple servers**.  
  
    If you choose **Target multiple servers**, designate the servers that will be targets for the job by checking the box to the left of the server name. Verify that the check boxes for servers that will not be targets of the job are unchecked.  
  
## <a name="TsqlProcedure"></a>Using Transact-SQL  
  
#### To modify the target servers for a job  
  
1.  Connect to the  Database Engine .  
  
2.  From the Standard bar, click **New Query**.  
  
3.  Copy and paste the following example into the query window and click **Execute**. This example assigns the multiserver job Weekly Sales Backups to the server SEATTLE2.  
  
```  
USE msdb ;  
GO  
  
EXEC dbo.sp_add_jobserver  
    @job_name = N'Weekly Sales Backups',   
    @server_name = N'SEATTLE2' ;   
GO  
```  
  
For more information, see [sp_add_jobserver (Transact-SQL)](assetId:///485252cc-0081-490a-9bd1-cbbd68eea286).  
  
## See Also  
[Automated Administration Across an Enterprise](../content/Automated-Administration-Across-an-Enterprise.md)  
  
