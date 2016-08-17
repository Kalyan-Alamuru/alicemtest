---
title: "SQLInstallTranslator Mapping"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bcd9ba4f-7834-4bc4-876e-c7478998e524
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLInstallTranslator Mapping
When an ODBC 2.*x* application calls **SQLInstallTranslator** through an ODBC 3*.x* driver, the Driver Manager maps the call to **SQLInstallTranslatorEx**.An application should not call **SQLInstallTranslator** in the ODBC 3*.x* Driver Manager with the *lpszInfFile* argument set to a value other than NULL. The ODBC.INF file used in ODBC 2.*x* is no longer supported in ODBC 3*.x*, even for backward compatibility.