---
title: "Interval Escape Sequences"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 303e8dab-8f13-4fa5-857f-15cc1f75bdd6
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Interval Escape Sequences
ODBC uses escape sequences for interval literals. The syntax of this escape sequence is as follows:  
  
 {*interval-literal*}  
  
 For the BNF syntax of *interval-literal*, see the [Interval Literal Syntax](../content/Interval-Literal-Syntax.md) section later in this appendix.  
  
 The interval literal escape sequence is supported if the interval data types are supported by the data source. An application should call **SQLGetTypeInfo** to determine whether these data types are supported.