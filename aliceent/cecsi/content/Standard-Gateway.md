---
title: "Standard Gateway"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b8341492-2141-4bab-80bd-f2752223079e
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Standard Gateway
A *gateway* is a piece of software that causes one DBMS to look like another. That is, the gateway accepts the programming interface, SQL grammar, and data stream protocol of a single DBMS and translates it to the programming interface, SQL grammar, and data stream protocol of the hidden DBMS. For example, applications written to use Microsoft® SQL Server™ can also access DB2 data through the Micro Decisionware DB2 Gateway; this product causes DB2 to look like SQL Server. When gateways are used, a different gateway must be written for each target database.  
  
 Although gateways are limited by architectural differences among DBMSs, they are a good candidate for standardization. However, if all DBMSs are to standardize on the programming interface, SQL grammar, and data stream protocol of a single DBMS, whose DBMS is to be chosen as the standard? Certainly no commercial DBMS vendor is likely to agree to standardize on a competitor's product. And if a standard programming interface, SQL grammar, and data stream protocol are developed, no gateway is needed.