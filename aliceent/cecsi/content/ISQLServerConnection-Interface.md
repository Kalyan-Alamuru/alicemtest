---
title: "ISQLServerConnection Interface"
ms.custom: na
ms.date: 07/18/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 031c01e2-2c65-4fe4-9700-fdbcc7a39f30
caps.latest.revision: 9
caps.handback.revision: 0
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
  - sv-se
  - zh-cn
  - zh-tw
---
# ISQLServerConnection Interface
  Represents a JDBC connection to a  Microsoft  SQL Server  database. This interface was added in  SQL Server  JDBC Driver 3.0.  
  
 **Package:** com.microsoft.sqlserver.jdbc  
  
 **Extends:** java.sql.Connection  
  
## Syntax  
  
```  
  
public interface ISQLServerConnection  
```  
  
## Remarks  
 This interface is implemented by [SQLServerConnection Class](../content/SQLServerConnection-Class.md).  
  
 This interface exposes the following  Microsoft JDBC Driver for SQL Server -specific field:  
  
|Field|For more information, see|  
|-----------|-------------------------------|  
|public final static int TRANSACTION_SNAPSHOT|[TRANSACTION_SNAPSHOT](../content/TRANSACTION_SNAPSHOT-Field--SQLServerConnection-.md)|  
|public UUID getClientConnectionId()|[getClientConnectionID()](../content/getClientConnectionID-Method--SQLServerConnection-.md)|  
  
## See Also  
 [JDBC Driver API Reference](../content/JDBC-Driver-API-Reference.md)  
  
  