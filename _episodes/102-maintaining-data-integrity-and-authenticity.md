---
title: Maintaining data integrity and authenticity
teaching: 10
exercises: 10
questions:
- What can we do to maintain data integrity and authenticity?
objectives:
- File naming concepts
- Conditions and use
- Data structure
- Data and structure documentation 

keypoints:
- Data integrity and authenticity is dependent on knowing what the data files contain, and who does what to what file. This requires both a findable, interpretable, and accessible file structure, an explicit file naming concept, knowledge of whom has access to what data, and documentation of data treatment procedures. 

---

"[life-cycle]: ../fig/101-intro/rdmkit-data-lifecycle.png"
"[life-cycle]: ../fig/101-intro/rdmkit-data-lifecycle.png"
"[life-cycle]: ../fig/101-intro/rdmkit-data-lifecycle.png"
"[life-cycle]: ../fig/101-intro/rdmkit-data-lifecycle.png"
"[life-cycle]: ../fig/101-intro/rdmkit-data-lifecycle.png"



> ## About this episode 
> Scientific results are no stronger than the data they are based on, and the data strength is dependent on its integrity and authenticity. Developing good practise for maintaining data integrity and authenticity is therefore essential to guarantee high quality results.

## Raw data
By raw data we mean collected or assembled data in a project that has not been subject to modifications, or removal of outliers. Raw data is data as we receive it after collection and before we start working on it. It is also the most important form of data, requiring special attention, as the quality of your raw data is decisive for the quality of all derived results. Alterations to raw data will affect all downstream results and may prevent reproducibility. 

Raw data should be treated in such a way that it:

* Has a clear and interpretable structure
* Prevents unintended modification
* Is clear who has read/write privileges
* Can be published and reused

## Versions of raw data
Imagine a data collection. The data is compiled in a file and given a file name. Some time later we want to add new data. We collect and add it to the original file. Even later we add a second layer of additional data. Three potential versions of our raw data now exist. Do we acknowledge all three as independent sets, or do we only recognise the latest? The answer depends on what data organisation strategy we apply!

- Single file + Internal documentation
All relevant information on what was added to the orignal data, and when, are stored in the data file itself and explained spatially or by labeling. Retrieval of the original data can be achieved based on the included information.

    Pros: One data file to keep track of. Information and data stored together
    Cons: May not be possible to extract versions of data without risk of introducing human error. May end up mixing data that should be stored separately (e.g. restricted vs. non-restricted data). Information added in file may disrupt data readability.

- Multiple files + External documentation
Each version of data is stored separately. All relevant information on what was added to the original data and when are stored in a separate (README-)file.

    Pros: Easy to identify file versions for specific uses. Data in file not obscured by non-data information. 
    Cons: Increased file management. Long term storage and publication of data can be complicated. 

## Analyses and code
Analyses and data modifications should be documented in such a way that your treatment and results are reproducible. For example:

- For results based on a subset of data
    * Documentation should describe how (and why) the data subset was selected from raw data and if the subset was subject to subsequent modifications prior to analysis
    * The analyses performed on the data subset should be described in such a way that the results are reproducible by others
    * Any script used should be stored in proximity with the results, referencing the data it was used on 

## Tabular data
A data spreadsheet is first and foremost a mode of data organisation. A common misconception is to treat a spreadsheet as a data file combined with a notebook, separating data and information based on visual distance and adding explanatory text notes in adjacent cells. From a human point of view, this makes sense. We want to visually see the information in a way we can relate to what we do with the data. From a computer perspective it makes little sense. It requires extensive explanation for a computer to interpret spreadsheet data the same way a human does.

Consider the spatial organisation of data even before you begin adding data to your spreadsheet. The spreadsheet consists of rows, columns, and cells. Make sure you:

1. Put all your **variables in columns** - The thing you're measuring, like 'Length', 'Attendance', or 'Gene'
2. Put each **observation in its own row** - The individual measures, like '180', 'Present', or 'MTND1-6'
3. **Do not combine multiple pieces of information in one cell** - Sometimes it just seems like one thing, but it is easier to later combine single cell information, than to separate combined data into single cells
4. Do not split combinable data in separate tables - Even if it makes sense from a human perspective, it can make export and analysis of your data unnecessarily complex.
5. Create a **data dictionary**! Explain, to yourself and future users, what column headers mean, the units of measure, if you use abbreviations, etc. Store the dictionary as a separate document in proximity to data. Avoid including the information in the data file! 
6. For storage, export and interoperability, export the cleaned data to a **text based format** like TSV, or CSV. This ensures that anyone can use the data, and is the format required by most data repositories.

An additional advice - If multiple contributors collect data in the same spreadsheet, make sure you enter the data in the same way. Having a spreadsheet containing data in multiple formats is a guarantee for errors and confusion! 

Things to avoid (at all costs!) when working with tabular data, is to enrich or visually enhance the data to facilitate human interpretation. Try to always avoid:

* Using colors to enhance cells
* Spatially distribute data more than necessary (computers prefer serially organised cells!)
* Mix data with analyses (Such as including data visualisations in Excel, e.g. Diagrams)
* Not treating null values (missing for humans is not equal to missing for a computer)

<!-- Images -->



For more in depth knowledge on spreadsheet clean-up we recommend the self guided exercise **here** <!-- add link to separate tabular data module -->

A more practical take on working with spreadsheet data is available in our **OpenRefine module** <!-- add link to OpenRefine module --> 

## Long term preservation of tabular data
Consider always saving binary data in alternative formats for long term storage or data archiving. This is especially true for tabular data. Proper file formats are CSV or TSV files, where data is stored with a minimal amount of formatting. It not only preserves the integrity of the data itself, but also reduces file sizes and increases data interoperability. Plain or enriched text can be read by most software on multiple platforms.


## File organisation
Any idea of organisation is better than no organisation! Organisation is often based on the concept of clustering, and clustering is often done either from a bottom-up or top-down perspective. 

Bottom up
Similar or related files tend to be kept together in folders. Folders are then clustered in super folders, etc.
Example: I collect my data in a folder, and create the analysis files in the same folder. I version my data in one or more parallel folders and run more analyses there. I then create a super folder for all data/analysis folders and begin working on my manuscript there.

Pros: Easy model for everyday work, intuitive clustering inspired by workflow.
Cons: Easy to lose overview. Files may end up in "wrong" folders. Creates clutter. 

Top down
Super folders are created first, then topic specific levels of sub folders. Clustering predates practise.
Example: I create an entire project folder structure, with several layers of sub folders for data, analyses, documentation etc. reflecting the project setup and workflow. When I generate data I place it in the data folder, make my analysis files in the analyses folder, and store my results in a separate folder. I begin working on my manuscript in a manuscript folder. 

Pros: Process defined file structure, follows the workflow. Ideal for third person view of project.
Cons: Rigid. Less flexible to work in with many folder levels, and movements between folders in workflow. Files may end up (temporarily) in wrong folder due to leisure.  

In practice, we may end up with a combination of top-down and bottom-up structures. Starting with a top-down approach, we may create new sub folders based on a bottom-up work flow. Any deviance from a plan is ok, as long as we keep track on what we do and why. When time comes to end a project, knowing where to find what can save a lot of time and effort.

Working in projects where data is shared among several collaborators, a pre-defined top-down file structure may not fit any single individual perfectly, but will likely benefit the greater good of the project most. It is a good idea to have one or two individuals responsible for overviewing and maintaining data structure in a shared project. A non-maintained file/folder structure can quickly become chaotic! 

## Etherpad exercise
Considering your own file structure, or the file structure used in your research group, write in the Etherpad: 

- If your current file structure is top-down or bottom-up, or a mix of the two. 
- Who the "inventor" of your file structure is (title, not name!), and to what extent you can influence how it is organized?
- One thing you believe you could improve in your current file structure.

### Three principles for (file) names:
<!--- Y: This section should be moved to File naming section --->
1. Machine readable – Avoid spaces, deliberate punctuation, accented characters, inconsistent letter casing
2. Human readable - A name describes the content of the file, connects to concept of a *slug* from semantic URLs<!--- Y: give an example of slug -->
3. Default ordering – Put something numeric first, use the ISO 8601 standard for dates (YYYYMMDD, or YYYY-MM-DD), left pad other numbers with zeros (01, 02, 03... 10)

## File naming
A file naming convention is a framework, or protocol, for naming your files in a way that describes the file contents and, importantly, how they relate to other files. Adopting a good file naming convention will increase file findability, making it easier to locate and search for in multiple combinations. 

A well suited file naming protocol should:

- Make it easy to understand what the file is and what it contains, from just reading the file name (Human readable)
    * Balance with the amount of elements: too many makes it difficult to understand vs. too few makes it general
    * Order the elements from general to specific
    * Use meaningful abbreviations
    * Use underscore (_), hyphen (-) or capitalized letters to separate elements in the name. Don’t use spaces or special characters: ?!& , * % # ; * ( ) @$ ^ ~ ‘ { } [ ] < >
    * Use date format ISO8601: YYYYMMDD, and time if needed HHMMSS, or in combination YYYYMMDD:HHMMSS
    * Include a version number if appropriate
    * Write your file naming convention down and explain abbreviations in your data documentation

Examples of good file names:

- Honeybee project, experiment 2 done in Helsinki, data file created on the second of December 2020
    * File name: 20201202_HB_EXP2_HEL_DATA_V03.xls
    * Explanation: Time_ProjectAbbreviation_ExperimentNumber_Location_TypeOfData_VersionNumber

- Cropped image of an ant head taken on the third of December 2020 by Meg Megson
    * 20201203_MM_HEAD_CROPPED_V1.psd
    * Time_CreatorData_TypeModification_Version

Examples of poor file names:
- Honeybee project, experiment 2 done in Helsinki, data file created on the second of December 2020
    * File name: Runnew_again_2NDTRY.xls
    * Explanation: N/A

- Cropped image of an ant head taken on the third of December 2020 by Meg Megson
    * Image_antclose_first_PUBLISHTHISONE3?.psd
    * N/A

- Any name like file.txt, file_new.txt, file_newer.txt, file_try.txt, file_add_new.txt etc.

### Bulk file names
Data producing equipment (and software) sometimes generate files with pre-defined names. These can be made up of a serial number or text string along with machine specific information. To a non-user such files can be incomprehensible, and may require explanation in order to make sense. To preserve the third-person view of files where the file name does not provide information of content or origin, sufficient documentation is required. Use sub-folders to cluster such files in manageable numbers and add README-files for orientation and explanation (Remember your future self!).

Sometimes continuous file name changes need to be done to generated data or analysis files. Manual modifications can be cumbersome and introduce typos. Consider using a bulk file name change tool to save time and prevent errors and maintain consistency.

Tools for bulk renaming
    * Mac - Renamer4Mac (Mac)
    * Windows - Bulk Rename Utility (Windows, free)
    * Windows/Mac/Linux - R

### Documentation of file organisation
Everyone knows their files and folders. A well documented file organisation where structure and hierarchy is explained may seem unnecessary to many, but can be an essential tool for the longevity of the data. There are two cases where this is particularly important:

- Shared projects
In any setting where data is shared in a research group or among colleagues a documented file system can act as a guarantee that files are handled in a similar fashion by all involved. In situations where some individuals are more focused on data production, and others on data analysis, an explicit description of what files goes where along with file contents, may act as safeguards for data integrity and authenticity.

- Project ending
Regardless of how many are involved in a project, at some time after it ends memory will start to fade on the specifics of file names and contents. Counting one's future self into the category of "third persons", a file structure documentation will be beneficial for when you need to go back to your data, or when someone else will reuse the data and/or results.

File structures are best explained and elaborated on in plain text README-files (plural). A good practice is to summarize the contents of folders on separate levels, trying to answer the question "What do someone else need to know about the contents of this folder in order to understand it?". Adding such knowledge will increase both data findability and reusability.


Example of folder structure and explanation in README.txt:

project/  
  code/                 code needed to go from input files to final results   
  data/                 raw and primary data (never edit!)   
     raw_external/  
     raw_internal/
     meta/  
  doc/                  documentation of the study  
  intermediate/         output files from intermediate analysis steps  
  logs/                 logs from the different analysis steps  
  notebooks/            notebooks that document your day-to-day work  
  results/              output from workflows and analyses  
     figures/  
     reports/  
     tables/  
  scratch/              temporary files that can safely be deleted or lost  
  README.txt            file and folder description  


### Conditions and use:
Knowing who does what to what, when it happens, and why, is essential in maintaining data integrity. If not already present, consider upgrading your file structure with an explicit 'Conditions and use' agreement, and apply it in file permissions. When considering raw data this is particularly important. Edits and changes to raw data should be restricted to only a few trusted individuals with particular responsibilities.

The same may be true for other files and folders as well. Large projects including many collaborators should have explicit permissions on file access. While it may seem democratic and trustful in allowing everyone equal access to everything, restricted access will reduce the risk of unintended mistakes and accidents.