---
title: "SET EXCLUSIVE Command"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d4fe12c5-7e8b-4d20-9ea4-2bcaffb271f2
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SET EXCLUSIVE Command
Specifies whether table files are opened for exclusive or shared use on a network.  
  
## Syntax  
  
```  
  
SET EXCLUSIVE ON | OFF  
```  
  
## Arguments  
 ON  
 Limits accessibility of a table opened on a network to the user who opened it. The table isn't accessible to other users on the network. SET EXCLUSIVE ON also prevents all other users from having read-only access.  
  
 OFF  
 (Default for the driver; the defaults for Visual FoxPro are ON for the global data session and OFF for a private data session.) Allows a table opened on a network to be shared and modified by any user on the network.  
  
## Remarks  
 Changing the setting of SET EXCLUSIVE doesn't change the status of previously opened tables. For example, if a table is opened with SET EXCLUSIVE set to ON and SET EXCLUSIVE is later changed to OFF, the table retains its exclusive-use status.  
  
## See Also  
 [ODBC Visual FoxPro Setup Dialog Box](../content/ODBC-Visual-FoxPro-Setup-Dialog-Box.md)