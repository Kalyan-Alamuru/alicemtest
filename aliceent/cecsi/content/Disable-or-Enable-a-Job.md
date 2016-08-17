---
title: "Disable or Enable a Job"
ms.custom: na
ms.date: 08/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5041261f-0c32-4d4a-8bee-59a6c16200dd
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
# Disable or Enable a Job
This topic describes how to disable a  SQL Server  Agent job in SQL Server 2016 by using SQL Server Management Studio or  Transact\-SQL . When you disable a job, it is not deleted and can be enabled again when necessary.  
  
**In This Topic**  
  
-   **Before you begin:**  
  
    [Security](#Security)  
  
-   **To disable or enable a job, using:**  
  
    [SQL Server Management Studio](#SSMS)  
  
    [Transact-SQL](#TSQL)  
  
## <a name="BeforeYouBegin"></a>Before You Begin  
  
### <a name="Security"></a>Security  
For detailed information, see [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMS"></a>Using SQL Server Management Studio  
  
#### To disable or enable a job  
  
1.  In **Object Explorer**, connect to an instance of the SQL Server Database Engine, and then expand that instance.  
  
2.  Expand **SQL Server Agent**.  
  
3.  Expand **Jobs**, and then right-click the job that you want to disable or enable.  
  
4.  To disable a job, click **Disable**. To enable a job, click **Enable**.  
  
## <a name="TSQL"></a>Using Transact-SQL  
  
#### To disable or enable a job  
  
1.  In **Object Explorer**, connect to an instance of  Database Engine .  
  
2.  On the Standard bar, click **New Query**.  
  
3.  Copy and paste the following example into the query window and click **Execute**.  
  
    ```  
    -- changes the name, description, and enables status of the job NightlyBackups.  
    USE msdb ;  
    GO  
  
    EXEC dbo.sp_update_job  
        @job_name = N'NightlyBackups',  
        @new_name = N'NightlyBackups -- Disabled',  
        @description = N'Nightly backups disabled during server migration.',  
        @enabled = 1 ;  
    GO  
    ```  
  
For more information, see [sp_update_job (Transact-SQL)](assetId:///cbdfea38-9e42-47f3-8fc8-5978b82e2623).  
  
