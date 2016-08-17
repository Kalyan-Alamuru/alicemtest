---
title: "Obtaining Descriptor Handles"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 936f983f-c7e9-43f3-97ea-dd4b1bbf4654
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Obtaining Descriptor Handles
An application obtains the handle of any explicitly allocated descriptor as an output argument of the call to **SQLAllocHandle**. The handle of an implicitly allocated descriptor is obtained by calling **SQLGetStmtAttr**.