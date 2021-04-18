---
title: Exporting data from spreadsheets
teaching: 10
exercises: 10
questions:
- What are examples of practices for converting data from spreadsheets to other file formats?

objectives:
- Understand what to consider when choosing data file formats
- Import and export tabular data in text-based file formats (CSV, TSV)
- Identify and address potential issues when importing or exporting from spreadsheets

keypoints:
- Use .csv file format for data storage and processing
- Be careful when using commas in values
---
> ## About this episode 
> All digital file formats are in danger of becoming outdated. If that happens, future software may not be able to read or show the information in the files correctly. In order to minimise the risk that files become unreadable, you should choose a file format that is likely to be usable in the future.
>
> 1. TOC
> {:toc}
> {: .toc}
{: .callout .toc}

## Good practices for selecting file formats
Software developers regularly release new versions of their products and it is not self-evident that the new software supports the use of files created with earlier software versions. Some software packages even disappear completely from the scene. Thus, all digital file formats are in danger of becoming outdated, and your choice of file formats should be planned carefully.

### Short-term data processing: file formats for operability
File format choice depends on your research phase. Choices for short-term data processing may differ from the choices you make for long-term data preservation.

For the reasons of short-term operability, it is advisable to choose a file format that is associated with the specific software that you intend to use for data analysis. Following discipline-specific standards and customs is generally the way to go. However, you should take into consideration how widespread these standards are and to what extent they will allow data processing by others than peers in your own discipline.

Proprietary file formats are owned and copyrighted by a specific company. Their specifications are usually not publicly available and their future development results from decisions and situation of their owner. Thus, the risk of obsolescence is high. However, some proprietary formats, such as Rich Text Format (*.rtf), MP3, MPEG, JPG, MS Excel (*.xls), SPSS (*.sav, *.por), STATA (*.dta) are widely used and you may assume that they will be useful for a reasonable time.

**Example**: We talked about how Excel stores **dates** as numbers in the previous episode. The numbers used to represent dates varies across versions of the software. In a scenario where you’re combining data stored in Excel Spreadsheets from multiple sources this could introduce a source of errors. 

### Long-term data preservation: file formats for the future
Standard, open and widespread formats are advisable for long-term storage as they typically undergo fewer changes. Contrary to proprietary formats (see above) specification of open formats is publicly available. Some of them are standardised and maintained by a standards organisation and we may assume that their readability in the future is ensured. Examples of open formats are PDF/A, CSV, TIFF, ASCII, Open Document Format (ODF), XML, Office Open XML, JPEG 2000, PNG, SVG, HTML, XHTML, RSS, CSS, etc.

**Tab-delimited** or **CSV** (more common) files are plain text files where the columns are separated by commas, hence 'comma separated variables' or CSV. The advantage of a CSV over an Excel/SPSS/etc. file is that we can open and read a CSV file using just about any software, including a simple **text editor**. Data in a CSV format can also be **easily imported** into other formats and environments, such as SQLite and R. Most spreadsheet programs can save to delimited text formats like CSV.

### Data conversion and possible data loss
It is advisable to store your data for use in the future, which means converting them from a current data format to a long-term preservation format. Most software applications offer export or exchange formats that allow a text-formatted file to be created for importing into another program. A typical example is Microsoft Excel, which through the 'Save As' command, can save spreadsheet data in comma delimited format (*.csv or comma separated values). The structure of the rows and columns is preserved through commas and line returns. However, multiple worksheets must be saved as separate *.csv files and any text formatting or macros in the native format will be lost on conversion.

> ### Discussion
> What are examples for information that may be lost when converting data between file formats?
>
>> ### Examples
>> - In the conversion of a statistical dataset (i.e. survey data), parts of the dataset may be lost, same as missing data definitions, decimal numbers, changes in data formats (e.g., numerical into string data type), data also may be truncated;
>> - In case of texts, i.e. transcriptions of speech, editing such as highlighting, bold texts, headers, footers may be lost;
>> - In case of images a reduction of resolution, loss of layer, colours may be lost;
>> - In converting audiovisual data file conversion may reduce sound quality;
>> - Some file formats are constructed specifically to save space. However, this is done by a reduction of information and data quality. For example, .jpg removes details from images, while .tiff bears full information. Similarly, .mp3 is a lossy format for audio data, while .wav keeps detailed information.
> {: .solution}
{: .discussion}

The conversion itself should be done by a researcher familiar with the data, so he or she can check for potential undesirable changes in the data that occurred as a result of the conversion.

Due to differences in national character sets you should pay attention also to character coding for text based file formats. Some coding systems (e.g., Windows 1250) do not cover all character sets at the same time. As a result, an adequate language environment (Central European languages) has to be set to ensure correct display, which cannot be done at all times. Other coding systems (e.g., UTF 8) allow correct display of symbols of several character sets simultaneously.

## How to work with text-based file formats in spreadsheets
To save a file you have opened in Excel in `*.csv` format:

1. Make sure that the tab your want to export is open
1. From the top menu select 'File' and 'Save as'.
1. In the 'Format' field, from the list, select 'Comma Separated Values' (`*.csv`).
1. Double check the file name and the location where you want to save it and hit 'Save'.

![Saving an Excel file to CSV](../fig/file-formats/excel-to-csv.png)

An important note for backwards compatibility: you can open CSVs in Excel!

> ### Exercise
>
> 1. Open the [training data spreadsheet](../data/training_attendance.xlsx)
> 1. Export the data under the tab `2016` in `*.csv` format
> 1. Open the `.csv` file in your text editor and compare it to the spreasheet
> 1. Open the `.csv` file in your spreadsheet software and compare  
> 1. What are the differences?
>
>> ### Examples from the section below
>> - The cells `RDM Training` and `Open access` no longer span the columns below them
>> - The bold face text formatting is lost
>> - The colored cells are lost
> {: .solution}
{: .challenge}


## How to address potential issues when importing or exporting from spreadsheets
However, there are some significant problems with this particular format. Quite often the data values themselves may include commas (,). In that case, the software which you use (including Excel) will most likely incorrectly display the data in columns. It is because the commas which are a part of the data values will be interpreted as a delimiter.

Data could look like this:

~~~
date,type,len_hours,num_registered,num_attended,trainer,cancelled
29 Apr,OA,1.5,1.5,15,JM,N
3 Mar,OA,60,19,25,PG,N
3 Jul,OA,1,25,20,PG, JM ,N
4 Jan,OA,1,26,17,JM,N
29 Mar,RDM,1,27,24,JM,N
~~~

Or like this if you're using the Swedish version:

~~~
date;type;len_hours;num_registered;num_attended;trainer;cancelled
29 apr;OA;1,5;1,5;15;JM;N
3 mar;OA;60;19;25;PG;N
3 jul;OA;1;25;20;PG; JM ;N
4 jan;OA;1;26;17;JM;N
29 mar;RDM;1;27;24;JM,N
~~~

> ### Note
> 
> Regional settings in Excel will influence the content of the CSV.
> The Swedish language version of Excel will use a semicolon as the separator instead of a comma.
> Excel functions that output localised text and numbers will also vary. The standard decimal separator in Swedish is a comma and names of months and days will appear as they do in your spreadsheet.
>
{: .callout}

In record `3 Jul,OA,1,25,20,PG, JM ,N` the value for *trainer* includes a comma for multiple trainers (`PG, JM`).
If we try to read the above into Excel (or other spreadsheet programme), we will get something like this:

![Issue with importing csv format](../fig/file-formats/csv-mistake.png)

The value for 'trainer' was split into two columns (instead of being put in one column `F`). This can propagate to a number of further errors. For example, the "extra" column will be interpreted as a column with many missing values (and without a proper header!).

If you want to store your data in `csv` format and expect that your data values may contain commas, you can avoid the problem discussed above by putting the values to be included in the same column in quotes (""). Applying this rule, the data might look like this:

~~~
date,type,len_hours,num_registered,num_attended,trainer,cancelled
29 Apr,OA,1.5,1.5,15,JM,N
3 Mar,OA,60,19,25,PG,N
3 Jul,OA,1,25,20,"PG, JM",N
4 Jan,OA,1,26,17,JM,N
29 Mar,RDM,1,27,24,JM,N
~~~

Now opening this file as a `csv` in Excel will not lead to an extra column, because Excel will only use commas that fall outside of quotation marks as delimiting characters. However, if you are working with an already existing dataset in which the data values are not included in "" but which have commas as both delimiters and parts of data values, you are potentially facing a major problem with data cleaning.

If the dataset you're dealing with contains hundreds or thousands of records, cleaning them up manually (by either removing commas from the data values or putting the values into quotes - "") is not only going to take hours and hours but may potentially end up with you accidentally introducing many errors.

Cleaning up datasets is one of the major problems in many scientific disciplines. The approach almost always depends on the particular context. However, it is a good practice to clean the data in an automated fashion, for example by writing and running a script.