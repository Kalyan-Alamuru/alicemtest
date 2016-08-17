---
title: "Jet 4.0 Uses SQL-92 Reserved Words List when ExtendedAnsiSQL_Set"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7645187e-7777-4c07-9686-0a80d5c5834d
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Jet 4.0 Uses SQL-92 Reserved Words List when ExtendedAnsiSQL_Set
When the ExtendedAnsiSQL flag is turned on, Jet 4.0 uses the SQL-92 reserved words list. Trying to use a SQL-92 reserved word as an unquoted object name will result in a syntax error. When the ExtendedAnsiSQL flag is turned off, the new reserved words can be used as object names as before.