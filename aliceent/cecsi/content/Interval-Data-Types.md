---
title: "Interval Data Types"
ms.custom: na
ms.date: 07/31/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fba93f65-c1db-44f4-91ba-532f87241cf7
caps.latest.revision: 6
manager: jhubbard
translation.priority.ht: 
  - en-gb
---
# Interval Data Types
An interval is defined as the difference between two dates and times. Intervals are expressed in one of two different ways. One is a *year-month* interval that expresses intervals in terms of years and an integral number of months. The other is a *day-time* interval that expresses intervals in terms of days, minutes, and seconds. These two types of intervals are distinct and cannot be mixed, because months can have varying numbers of days.  
  
 An interval consists of a set of fields. There is an implied ordering among the fields. For example, in a year-to-month interval, the year comes first, followed by the month. Similarly, in a day-to-minute interval, the fields are in the order day, hour, and minute. The first field in an interval type is called the *leading* field, or the *high-order* field. The last field is called the *trailing* field.  
  
 In all intervals, the leading field is not constrained by rules of the Gregorian calendar. For example, in an hour-to-minute interval, the hour field is not constrained to be between 0 and 23 (inclusive), as it normally is. The trailing fields subsequent to the leading field follow the usual constraints of the Gregorian calendar. For more information, see [Constraints of the Gregorian Calendar](../content/Constraints-of-the-Gregorian-Calendar.md), later in this appendix.  
  
 There are 13 interval SQL data types and 13 interval C data types. Each of the interval C data types uses the same structure, SQL_INTERVAL_STRUCT, to contain the interval data. (For more information, see the next section, [C Interval Structure](../content/C-Interval-Structure.md).) For more information on the SQL data types, see [SQL Data Types](../content/SQL-Data-Types.md); for more information on the C data types, see [C Data Types](../content/C-Data-Types.md).  
  
|Type identifier|Class|Description|  
|---------------------|-----------|-----------------|  
|MONTH|Year-Month|Number of months between two dates.|  
|YEAR|Year-Month|Number of years between two dates.|  
|YEAR_TO_MONTH|Year-Month|Number of years and months between two dates.|  
|DAY|Day-Time|Number of days between two dates.|  
|HOUR|Day-Time|Number of hours between two date/times.|  
|MINUTE|Day-Time|Number of minutes between two date/times.|  
|SECOND|Day-Time|Number of seconds between two date/times.|  
|DAY_TO_HOUR|Day-Time|Number of days/hours between two date/times.|  
|DAY_TO_MINUTE|Day-Time|Number of days/hours/minutes between two date/times.|  
|DAY_TO_SECOND|Day-Time|Number of days/hours/minutes/seconds between two date/times.|  
|HOUR_TO_MINUTE|Day-Time|Number of hours/minutes between two date/times.|  
|HOUR_TO_SECOND|Day-Time|Number of hours/minutes/seconds between two date/times.|  
|MINUTE_TO_SECOND|Day-Time|Number of minutes/seconds between two date/times.|  
  
 This section contains the following topics.  
  
-   [C Interval Structure](../content/C-Interval-Structure.md)  
  
-   [Interval Data Type Precision](../content/Interval-Data-Type-Precision.md)  
  
-   [Interval Data Type Length](../content/Interval-Data-Type-Length.md)  
  
-   [Interval Literals](../content/Interval-Literals.md)  
  
-   [Overriding Default Leading and Seconds Precision for Interval Data Types](../content/Overriding-Default-Leading-and-Seconds-Precision-for-Interval-Data-Types.md)