---
title: "Setting ExtendedAnsiSQL"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 37b775d1-65ac-45ac-8572-454bc4e3c1a2
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Setting ExtendedAnsiSQL
The attribute can be controlled in the connection string by adding the ExtendedAnsiSQL attribute:  
  
|Value|Description|  
|-----------|-----------------|  
|ExtendedAnsiSQL=0 (default)|This setting does not enable the new features.|  
|ExtendedAnsiSQL=1|This setting enables the new features.|  
  
 The attribute can also be set in a DSN through the **Advanced Options** dialog box when configuring a DSN through Control Panel.  
  
 Setting the attribute to 0 disables the new features; setting it to 1 enables the new features.  
  
 The attribute can also be set using SQLSetConnectAttr(). The attribute value is 65501 and is set to a SQLINTEGER value of 1 or 0, as documented in the preceding table. It can be called before or after connecting, but it is better to call it after connecting because of the order in which the driver processes cached connection attributes and connection strings.