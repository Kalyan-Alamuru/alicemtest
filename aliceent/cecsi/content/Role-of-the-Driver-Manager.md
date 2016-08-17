---
title: "Role of the Driver Manager"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7b861c82-357e-4590-8074-45136e9ed15e
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Role of the Driver Manager
The Driver Manager determines the final order in which to return status records that it generates. In particular, it determines which record has the highest rank and is to be returned first. The driver is responsible for ordering status records that it generates. If status records are posted by both the Driver Manager and the driver, the Driver Manager is responsible for ordering them. For more information, see [Sequence of Status Records](../content/Sequence-of-Status-Records.md).  
  
 The Driver Manager does as much error checking as it can. This saves every driver from checking for the same errors. For example, if a function argument accepts a discrete number of values, such as *Operation* in **SQLSetPos**, the Driver Manager checks that the specified value is legal.  
  
 The following sections describe the types of conditions checked by the Driver Manager. They are not intended to be exhaustive; for a complete list of the SQLSTATEs the Driver Manager returns, see the "Diagnostics" section of each function; the description of each check made by the Driver Manager starts with the letters "(DM)." Also see the state transition tables in [Appendix B: ODBC State Transition Tables](../Topic/Appendix%20B:%20ODBC%20State%20Transition%20Tables.md); errors shown in parentheses are detected by the Driver Manager.  
  
 This section contains the following topics.  
  
-   [Argument Value Checks](../content/Argument-Value-Checks.md)  
  
-   [State Transition Checks](../content/State-Transition-Checks.md)  
  
-   [General Error Checks](../content/General-Error-Checks.md)  
  
-   [Driver Manager Error and Warning Checks](../content/Driver-Manager-Error-and-Warning-Checks.md)