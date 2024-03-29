---
layout: default
title: Dates as Data
parent: Workshop Content
nav_order: 4
---

## Date formats in spreadsheets

Dates in spreadsheets are often stored in a single column. 

While this seems like a logical way to record dates when you are entering them, or visually reviewing data, it's not actually a best practice for preparing data for analysis.

When working with data, your goal is to have as little ambiguity as possible. Ambiguity can creep into your data when working with dates when there are regional variations either in your observations and when you or your team might be working with different versions or suites of software products (e.g., LibreOffice, Microsoft Excel, Gnumeric).

## Regional date formatting

When you enter a date into a spreadsheet it looks like a date although the spreadsheet program may
display different text from what you input. It does this to be 'helpful' but it often is not. 

For example if you enter '7/12/88' into your
Excel spreadsheet it may display as '07/12/1988' (depending on your version of Excel). These
are different ways of formatting the same date.

Different countries also write dates differently. If you are in the UK, for example, you will interpret
the date above as the 7th day of December, however a researcher from the US will interpret the same entry as the 12th day of July. This regional variation is handled automatically by your
spreadsheet program so that when you are typing in dates they appear as you would expect. If you
try to type in a US format date into a UK version of Excel, it may or may not be treated as a
date.

It is therefore a good idea to treat dates, not as a single data point, but as
three distinct pieces of data (month, day, and year). Separating dates into their component parts
will avoid this confusion, while also giving the added benefit of allowing you to compare, for
example data collected in January of multiple years with data collected in February of multiple years.

## Dates stored as integers

One of the other reasons dates can be tricky is that most spreadsheet programs have “useful features” which can change the way dates are displayed - but not stored. The image below demonstrates some of the many date formatting options in Excel. 

![Many formats, many ambiguities](../fig/excel_dates_1.jpg)

Excel stores dates as serial numbers (see last column above). This serial number represents the number of days from December 31, 1899. In the example, July 2, 2014 is stored as the serial number 41822.

**Excel's date systems:** Excel also entertains a second date system, the 1904 date system, as the default in Excel for Macintosh. This system will assign a different serial number than the [1900 date system](https://support.microsoft.com/en-us/help/214330/differences-between-the-1900-and-the-1904-date-system-in-excel). Because of this, dates must be checked for accuracy when exporting data from Excel (look for dates that are ~4 years off).
{: .note}

### Activity 1: Separating dates into components

Step 1
{: .label .label-step}
Download and open the [SAFI_dates.xlsx](https://ndownloader.figshare.com/files/11502827) file. This file contains a subset of the data from the SAFI interviews, including the dates on which the interviews were conducted.
{: .step}

Step 2
{: .label .label-step}
Choose the tab of the spreadsheet that corresponds to the way you format dates in your location (either day first `DD_MM_YEAR`, or month first `MM_DD_YEAR`). Extract the components of the date to new columns. For this we can use the built in Excel functions:
`=MONTH()`    
`=DAY()`  
`=YEAR()`
{: .step}

Step 3
{: .label .label-step}
Apply each of these formulas to its entire column. Make sure the new column is formatted as a number and not as a date.
{: .step}

Your spreadsheet should look like this (Note that this solution shows the dates in `MM_DD_YEAR` format):
![dates exercise 1](../fig/solution_exercise_1_dates.png)

We now have each component of our date isolated in its own column. This will allow us to group our data with respect to month, year, or day of month for our analyses and will also prevent problems when passing data between different versions of spreadsheet software (as for example when sharing data with collaborators in different countries).


### Activity 2: Default year

Step 1
{: .label .label-step}
Using the same spreadsheet you used for the previous exercise, add another data point in the `interview_date` column by typing either `11/17` (if your location uses `MM/DD` formatting) or `17/11` (if your location uses `DD/MM` formatting). The `Day`, `Month`, and `Year` columns should populate for this new data point. What year is shown in the `Year` column?
{: .step}

<details>
  <summary><b>Solution</b></summary>
<br>
If no year is specified, the spreadsheet program will assume you mean the current year and will insert that value. This may be incorrect if you are working with historical data so be very cautious when working with data that does not have a year specified within its date variable.
</details>

## Historical data
Excel is unable to parse dates from before 1899-12-31, and will thus leave these untouched.  If you’re mixing historic data
from before and after this date, Excel will translate only the post-1900 dates into its internal format, thus resulting in mixed data. If you’re working with historic data, be extremely careful with your dates!
