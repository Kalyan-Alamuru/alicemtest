---
title: "Using the VFP FoxPro ODBC Driver with Your Visual Basic Application"
ms.custom: na
ms.date: 07/29/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5223ca23-5df6-4ebc-aa3b-70682ff27a8c
caps.latest.revision: 5
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Using the VFP FoxPro ODBC Driver with Your Visual Basic Application
Your Microsoft® Visual Basic® application can communicate with Visual FoxPro data by creating a data control that connects to a Visual FoxPro data source.  
  
#### To connect to Visual FoxPro data using the Data Control in Visual Basic  
  
1.  Create a data source named "test" that connects to the TasTrade sample database included in Visual FoxPro. The default Visual FoxPro installation places the TasTrade sample database in the location:  
  
    ```  
    c:\vfp\samples\mainsamp\data\tastrade.dbc  
    ```  
  
2.  In Visual Basic, create a new form and place a text box and a Data control on it.  
  
3.  Change the Data control's Connect property as follows:  
  
    ```  
    ODBC;DATABASE=tastrade;DSN=test  
    ```  
  
4.  Change the RecordsetType property to the following:  
  
    ```  
    2 - Snapshot  
    ```  
  
5.  Change the RecordSource property to the following:  
  
    ```  
    customer  
    ```  
  
6.  Change the DataSource property for the text box to the default name for the Data control to the following:  
  
    ```  
    data1  
    ```  
  
7.  Change the text box's DataField property to the following:  
  
    ```  
    customer_id  
    ```  
  
8.  Run the form, and use the Data control to skip through the customer id fields from the Visual FoxPro TasTrade sample database.