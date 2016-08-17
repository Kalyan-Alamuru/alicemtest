---
title: "Interface Conformance Levels"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2c470e54-0600-4b2b-b1f3-9885cb28a01a
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Interface Conformance Levels
The purpose of leveling is to inform the application what features are available to it from the driver. A leveling scheme based on functions does not sufficiently achieve this goal. In ODBC 3.*x*, drivers are classified based on the features they possess. Supporting the feature can include supporting the function; it can also include supporting a descriptor field, a statement attribute, a "Y" value for an information type returned by **SQLGetInfo**, and so on.  
  
 To simplify specification of interface conformance, ODBC defines three conformance levels. To meet a particular conformance level, a driver must satisfy all of the requirements of that conformance level. Conformance with a given level implies complete conformance with all lower levels.  
  
 Conformance levels do not always divide neatly into support for a specific list of ODBC functions, but specify supported features as listed in the following sections. To provide support for a feature, a driver must support some or all forms of calls to certain ODBC functions (for more information, see [Function Conformance](../content/Function-Conformance.md)), setting certain attributes (see [Attribute Conformance](../content/Attribute-Conformance.md)), and certain descriptor fields (see [Descriptor Field Conformance](../content/Descriptor-Field-Conformance.md)).  
  
 The application discovers a driver's interface conformance level by connecting to a data source and calling **SQLGetInfo** with the SQL_ODBC_INTERFACE_CONFORMANCE option.  
  
 Drivers are free to implement features beyond the level to which they claim complete conformance. Applications discover any such additional capabilities by calling **SQLGetFunctions** (to determine which ODBC functions are present) and **SQLGetInfo** (to query various other ODBC capabilities).  
  
 There are three ODBC interface conformance levels: Core, Level 1, and Level 2.  
  
> [!NOTE]  
>  These conformance levels have different requirements than the ODBC API conformance levels of the same name in ODBC 2*.x*. In particular, all the features implied by ODBC 2*.x* API conformance Level 1 are now part of the Core interface conformance level. As a result, many ODBC drivers may report Core-level interface conformance.  
  
 This section contains the following topics.  
  
-   [Core Interface Conformance](../content/Core-Interface-Conformance.md)  
  
-   [Level 1 Interface Conformance](../content/Level-1-Interface-Conformance.md)  
  
-   [Level 2 Interface Conformance](../content/Level-2-Interface-Conformance.md)  
  
-   [Function Conformance](../content/Function-Conformance.md)  
  
-   [Attribute Conformance](../content/Attribute-Conformance.md)  
  
-   [Descriptor Field Conformance](../content/Descriptor-Field-Conformance.md)