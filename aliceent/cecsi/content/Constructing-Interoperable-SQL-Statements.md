---
title: "Constructing Interoperable SQL Statements"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dee6f7e2-bcc4-4c74-8c7c-12aeda8a90eb
caps.latest.revision: 7
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Constructing Interoperable SQL Statements
As mentioned in the previous sections, interoperable applications should use the ODBC SQL grammar. Beyond using this grammar, however, a number of additional problems are faced by interoperable applications. For example, what does an application do if it wants to use a feature, such as outer joins, that is not supported by all data sources?  
  
 At this point, the application writer must make some decisions about which language features are required and which are optional. In most cases, if a particular driver does not support a feature required by the application, the application simply refuses to run with that driver. However, if the feature is optional, the application can work around the feature. For example, it might disable those parts of the interface that allow the user to use the feature.  
  
 To determine which features are supported, applications start by calling **SQLGetInfo** with the SQL_SQL_CONFORMANCE option. The SQL conformance level gives the application a broad view of which SQL is supported. To refine this view, the application calls **SQLGetInfo** with any of a number of other options. For a complete list of these options, see the [SQLGetInfo](../content/SQLGetInfo-Function.md) function description. Finally, **SQLGetTypeInfo** returns information about the data types supported by the data source. The following sections list a number of possible factors that applications should watch for when constructing interoperable SQL statements.  
  
 This section contains the following topics.  
  
-   [Catalog and Schema Usage](../content/Catalog-and-Schema-Usage.md)  
  
-   [Catalog Position](../content/Catalog-Position.md)  
  
-   [Quoted Identifiers](../content/Quoted-Identifiers.md)  
  
-   [Identifier Case](../content/Identifier-Case.md)  
  
-   [Escape Sequences](../content/Escape-Sequences.md)  
  
-   [Literal Prefixes and Suffixes](../content/Literal-Prefixes-and-Suffixes.md)  
  
-   [Parameter Markers in Procedure Calls](../content/Parameter-Markers-in-Procedure-Calls.md)  
  
-   [DDL Statements](../content/DDL-Statements.md)