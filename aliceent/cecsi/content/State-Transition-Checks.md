---
title: "State Transition Checks"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0706db7d-e125-4845-a13a-7fe4308f7360
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# State Transition Checks
The Driver Manager checks that the state of the environment, connection, or statement is appropriate for the function being called. For example, a connection must be in an allocated state when **SQLConnect** is called; a statement must be in a prepared state when **SQLExecute** is called. The Driver Manager returns SQL_ERROR for state transition errors.