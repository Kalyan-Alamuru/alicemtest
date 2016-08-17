---
title: "Importing Data into Microsoft Excel from a Visual FoxPro Database"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3085bc4c-00a7-40e5-bffb-c3962cd3d509
caps.latest.revision: 7
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Importing Data into Microsoft Excel from a Visual FoxPro Database
You can import Visual FoxPro data into your Microsoft Excel worksheet if you have defined a data source for it. For information about creating a Visual FoxPro data source, see [Accessing a Visual FoxPro Data Source from Microsoft Excel](../content/Accessing-a-Visual-FoxPro-Data-Source-from-Microsoft-Excel.md).  
  
### To import Visual FoxPro data into an Microsoft Excel worksheet  
  
1.  Open a Microsoft Excel spreadsheet.  
  
2.  From the Data menu, choose Get External Data. Microsoft Query opens.  
  
3.  In the Select Data Source dialog box, select a Visual FoxPro data source and then click Use.  
  
4.  If the database accessed by your data source includes tables, select a table from the Add Tables dialog box. Microsoft Query displays the added table in the top half of the query designer.  
  
    > [!NOTE]  
    >  The Owner list is not available in this dialog box because the driver does not support owners. The Database list is not available because the driver does not support multiple databases in a data source.  
  
5.  Select fields for your query by dragging them from the table onto the lower half of the designer.  
  
6.  Close Microsoft Query. The data you selected is imported into your Microsoft Excel spreadsheet.