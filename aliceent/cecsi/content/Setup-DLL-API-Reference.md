---
title: "Setup DLL API Reference"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f9d03f17-1c0d-4e7c-9c04-8c316e07ef25
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Setup DLL API Reference
This section describes the syntax of the driver setup DLL API,which consists of two functions (**ConfigDriver** and **ConfigDSN**). **ConfigDriver** and **ConfigDSN** can be either in the driver DLL or in a separate setup DLL.  
  
 In addition, this section describes the syntax of the translator setup DLL API, which consists of a single function (**ConfigTranslator**). **ConfigTranslator** can be either in the translator DLL or in a separate setup DLL.  
  
 Each function is labeled with the version of ODBC in which it was introduced.  
  
 This section contains the following topics.  
  
-   [ConfigDriver Function](../content/ConfigDriver-Function.md)  
  
-   [ConfigDSN Function](../content/ConfigDSN-Function.md)  
  
-   [ConfigTranslator Function](../content/ConfigTranslator-Function.md)