---
title: "SQLGetDiagRec Function"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLGetDiagRec
apilocation: 
  - sqlsrv32.dll
apitype: dllExport
ms.assetid: ebdbac93-3d68-438f-8416-ef1f08e04269
caps.latest.revision: 26
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# SQLGetDiagRec Function
**Conformance**  
 Version Introduced: ODBC 3.0 Standards Compliance: ISO 92  
  
 **Summary**  
 **SQLGetDiagRec** returns the current values of multiple fields of a diagnostic record that contains error, warning, and status information. Unlike **SQLGetDiagField**, which returns one diagnostic field per call, **SQLGetDiagRec** returns several commonly used fields of a diagnostic record, including the SQLSTATE, the native error code, and the diagnostic message text.  
  
## Syntax  
  
```  
  
SQLRETURN SQLGetDiagRec(  
     SQLSMALLINT     HandleType,  
     SQLHANDLE       Handle,  
     SQLSMALLINT     RecNumber,  
     SQLCHAR *       SQLState,  
     SQLINTEGER *    NativeErrorPtr,  
     SQLCHAR *       MessageText,  
     SQLSMALLINT     BufferLength,  
     SQLSMALLINT *   TextLengthPtr);  
```  
  
## Arguments  
 *HandleType*  
 [Input] A handle type identifier that describes the type of handle for which diagnostics are required. Must be one of the following:  
  
-   SQL_HANDLE_DBC  
  
-   SQL_HANDLE_DBC_INFO_TOKEN  
  
-   SQL_HANDLE_DESC  
  
-   SQL_HANDLE_ENV  
  
-   SQL_HANDLE_STMT  
  
 SQL_HANDLE_DBC_INFO_TOKEN handle is used only by the Driver Manager and driver. Applications should not use this handle type. For more information about SQL_HANDLE_DBC_INFO_TOKEN, see [Developing Connection-Pool Awareness in an ODBC Driver](../content/Developing-Connection-Pool-Awareness-in-an-ODBC-Driver.md).  
  
 *Handle*  
 [Input] A handle for the diagnostic data structure, of the type indicated by *HandleType*. If *HandleType* is SQL_HANDLE_ENV, *Handle* can be either a shared or an unshared environment handle.  
  
 *RecNumber*  
 [Input] Indicates the status record from which the application seeks information. Status records are numbered from 1.  
  
 *SQLState*  
 [Output] Pointer to a buffer in which to return a five-character SQLSTATE code (and terminating NULL) for the diagnostic record *RecNumber*. The first two characters indicate the class; the next three indicate the subclass. This information is contained in the SQL_DIAG_SQLSTATE diagnostic field. For more information, see [SQLSTATEs](../content/SQLSTATEs.md).  
  
 *NativeErrorPtr*  
 [Output] Pointer to a buffer in which to return the native error code, specific to the data source. This information is contained in the SQL_DIAG_NATIVE diagnostic field.  
  
 *MessageText*  
 [Output] Pointer to a buffer in which to return the diagnostic message text string. This information is contained in the SQL_DIAG_MESSAGE_TEXT diagnostic field. For the format of the string, see [Diagnostic Messages](../content/Diagnostic-Messages.md).  
  
 If *MessageText* is NULL, *TextLengthPtr* will still return the total number of characters (excluding the null-termination character for character data) available to return in the buffer pointed to by *MessageText*.  
  
 *BufferLength*  
 [Input] Length of the **MessageText* buffer in characters. There is no maximum length of the diagnostic message text.  
  
 *TextLengthPtr*  
 [Output] Pointer to a buffer in which to return the total number of characters (excluding the number of characters required for the null-termination character) available to return in *\*MessageText*. If the number of characters available to return is greater than *BufferLength*, the diagnostic message text in *\*MessageText* is truncated to *BufferLength* minus the length of a null-termination character.  
  
## Returns  
 SQL_SUCCESS, SQL_SUCCESS_WITH_INFO, SQL_ERROR, or SQL_INVALID_HANDLE.  
  
## Diagnostics  
 **SQLGetDiagRec** does not post diagnostic records for itself. It uses the following return values to report the outcome of its own execution:  
  
-   SQL_SUCCESS: The function successfully returned diagnostic information.  
  
-   SQL_SUCCESS_WITH_INFO: The \**MessageText* buffer was too small to hold the requested diagnostic message. No diagnostic records were generated. To determine that a truncation occurred, the application must compare *BufferLength* to the actual number of bytes available, which is written to **StringLengthPtr*.  
  
-   SQL_INVALID_HANDLE: The handle indicated by *HandleType* and *Handle* was not a valid handle.  
  
-   SQL_ERROR: One of the following occurred:  
  
    -   *RecNumber* was negative or 0.  
  
    -   *BufferLength* was less than zero.  
  
    -   When using asynchronous notification, the asynchronous operation on the handle was not complete.  
  
-   SQL_NO_DATA: *RecNumber* was greater than the number of diagnostic records that existed for the handle specified in *Handle.* The function also returns SQL_NO_DATA for any positive *RecNumber* if there are no diagnostic records for *Handle*.  
  
## Comments  
 An application typically calls **SQLGetDiagRec** when a previous call to an ODBC function has returned SQL_ERROR or SQL_SUCCESS_WITH_INFO. However, because any ODBC function can post zero or more diagnostic records each time it is called, an application can call **SQLGetDiagRec** after any ODBC function call. An application can call **SQLGetDiagRec** multiple times to return some or all of the records in the diagnostic data structure. ODBC imposes no limit to the number of diagnostic records that can be stored at any one time.  
  
 **SQLGetDiagRec** cannot be used to return fields from the header of the diagnostic data structure. (The *RecNumber* argument must be greater than 0.) The application should call **SQLGetDiagField** for this purpose.  
  
 **SQLGetDiagRec** retrieves only the diagnostic information most recently associated with the handle specified in the *Handle* argument. If the application calls another ODBC function, except **SQLGetDiagRec**, **SQLGetDiagField**, or **SQLError**, any diagnostic information from the previous calls on the same handle is lost.  
  
 An application can scan all diagnostic records by looping, incrementing *RecNumber*, as long as **SQLGetDiagRec** returns SQL_SUCCESS. Calls to **SQLGetDiagRec** are nondestructive to the header and record fields. The application can call **SQLGetDiagRec** again at a later time to retrieve a field from a record as long as no other function, except **SQLGetDiagRec**, **SQLGetDiagField**, or **SQLError**, has been called in the interim. The application can also retrieve a count of the total number of diagnostic records available by calling **SQLGetDiagField** to retrieve the value of the SQL_DIAG_NUMBER field, and then calling **SQLGetDiagRec** that many times.  
  
 For a description of the fields of the diagnostic data structure, see [SQLGetDiagField](../content/SQLGetDiagField-Function.md). For more information, see [Using SQLGetDiagRec and SQLGetDiagField](../content/Using-SQLGetDiagRec-and-SQLGetDiagField.md) and [Implementing SQLGetDiagRec and SQLGetDiagField](../content/Implementing-SQLGetDiagRec-and-SQLGetDiagField.md).  
  
 Calling an API other than the one that’s being executed asynchronously will generate HY010 "Function sequence error". However, the error record cannot be retrieved before the asynchronous operation completes.  
  
## HandleType Argument  
 Each handle type can have diagnostic information associated with it. The *HandleType* argument denotes the handle type of the *Handle* argument.  
  
 Some header and record fields cannot be returned for environment, connection, statement, and descriptor handles. Those handles for which a field is not applicable are indicated in the "Header Fields" and "Record Fields" sections in [SQLGetDiagField](../content/SQLGetDiagField-Function.md).  
  
 A call to **SQLGetDiagRec** will return SQL_INVALID_HANDLE if *HandleType* is SQL_HANDLE_SENV, which denotes a shared environment handle. However, if *HandleType* is SQL_HANDLE_ENV, *Handle* can be either a shared or an unshared environment handle.  
  
## Related Functions  
  
|For information about|See|  
|---------------------------|---------|  
|Obtaining a field of a diagnostic record or a field of the diagnostic header|[SQLGetDiagField Function](../content/SQLGetDiagField-Function.md)|  
  
## See Also  
 [ODBC API Reference](../content/ODBC-API-Reference.md)   
 [ODBC Header Files](../content/ODBC-Header-Files.md)   
 [Sample ODBC Program](../content/Sample-ODBC-Program.md)