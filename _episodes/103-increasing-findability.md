---
title: Maintaining data integrity and authenticity
teaching: 10
exercises: 10
questions:
- What can we do to maintain data integrity and authenticity?
objectives:
- Incresing file findability
- File naming concepts
- The concept of tagging files with metadata 

keypoints:
- File findability is connected to the future value of research
- Meta tagging files with relevant information increases findability
- Avoid creating unnecessary folders by use of smart folders 

---

> ## About this episode 
>A key point in data management is finding information among large sets of files and data. Knowing all your files and their contents can be a manageable method in the short term, but as files and folders increase in size and numbers and old projects are replaced with new ones, the once clear overview is obscured and finding specific information becomes harder. Suddenly you begin to struggle finding files you know exist, or critical decisions are difficult to make due to information overload or a paralysing mass of irrelevant files/folders/data.

## What is the problem with file findability?
When we think about findability we often make implicit analogies to search engines. Type in what you want to find in a specific application (e.g. web browser) and quickly obtain a list of search results. The problem with this analogy is that a web browser is used to find information that was created with the sole purpose of being found! Working with research data requires us to think differently.

When we collect data and organise it for research purposes, findability is not necessarily our primary, or even a significant, motivation. 
 
## Multiple file copies
One way to increase findability is to make copies of files used in separate contexts and store these in process specific locations. A part of this process may even include renaming duplicated files in a way that fits the new context. For each context a new copy of a file is made and stored separately. The risks with such a procedure should be obvious to everyone. The same also applies to collaborations lacking common storage and working spaces. Files may be distributed among project participants by mail or by using portable devices (Flash drives, hard drives, etc.), creating situations where multiple copies exist simultaneously.

Pros: Someone is (always?) guaranteed to have the latest version of a file!
Cons: Who has the latest version of a file?

While such a system may seem feasible at first, the amount of administration to keep track of distribution schemes and file edits will quickly outweigh the benefits.

Any system dependent on tracking the use of multiple file copies is strongly advised against! 

## File shortcuts
Shortcuts are an easy, feasible, and intuitive way to increase findability while avoiding file duplications. A shortcut can point to a file location anywhere, even on a network drive.

Pros: Easy to create, file name of shortcut can be changed without compromising the original file integrity and may even increase findability when named differently.  
Cons: Shortcut may break if original file location or name is changed. Easy to lose orientation if not maintained regularly. 

## Increasing file findability?
What are good practices for increasing file findability? The answer is somewhat dependent on context. With findability we do not only mean finding files and folders on your individual laptop. Findability encompasses the ability to find a file independent of the number of individuals it concerns, operating system(s) used, number of collaboration platforms, or time. Findability is **per se** a quality in itself, and is first and foremost based on the file name properties. The most important way to find the file you are looking for is via its file name. However, there are more ways we can work with findability.

- Metadata
A good and informative file name is a great start, but there is a limit to how much information you can pack into a file name before the length itself becomes a problem. This is where metadata comes in. For the purpose of findability we can associate the file name with metadata stored elsewhere, for example in a text file kept together with the files.

An example:
20220115_MyFile_Project1_Location_Dataiteration1_V1.xml

project/  
  files/                   
    20220115_MyFile_Project1_Location_Dataiteration1_V1.xml
    20220115_MyFile_Project1_Location_Dataiteration2.xml
    Metadata.txt
      "20220115_MyFile_Project1_Location_Dataiteration1_V1.xml 
      Contains X data from Y, with additions of Z made by A and B on 20220110 including suggestions by C.
      20220115_MyFile_Project1_Location_Dataiteration2.xml
      Contains X data from Y, with additions of Z made only by A on 20220111 not including suggestions by C."

In this case the Metadata.txt lists the file name and associates it with additional data not possible to squeeze into the file name itself. By adding it separately and associating it with the file name we increase findability by a lot.

- Tagging
While metadata can be added separately it is first and foremost descriptive of the file contents and interpretability. The final layer to increasing findability is by tagging the metadata with specific keywords. For a wide selection of files used in a specific context, but stored in separate locations, adding keywords will tie the file together.

For the daily routine in working with data it all seems a bit over the top to combine file naming conventions with both metadata files and tagging, but your future self (and others) may be eternally grateful!

project/  
  files/                   
    20220115_MyFile_Project1_Location_Dataiteration1_V1.xml
    Metadata.txt
      "20220115_MyFile_Project1_Location_Dataiteration1_V1.xml Contains X data from Y, with additions of Z made by A and B on 20220110 not including suggestions by C.
      Keyword HumptyDumpty"


#### How to encode/extract metadata from filenames

Deliberately use "-" and "_" to allow recovery of meta-data from the filenames:

- "_" underscore used to delimit units of meta-data to be used in searches.
- "-" hyphen used to delimit words to increase readability.

## Exercise - File Organisation

Download the compressed file [File name] from [Download location] and unzip on your laptop. The file contains a collection of files from an imaginary project, somewhat resembling what the initial phase of a project can look like. Given the files provided:

- Create a proper hierarchical folder system based on the file names and contents
- Rename files in a consistent manner if required, such that it reflects both contents and file version  
- Optionally, create a file for meta tagging files with keywords according to file contents


<!--- Skriv om delmomentet utifrån begränsningar i hierakiskt filsystem --->

```
 10_final-figs-for-publication.R
 1_data-cleaning.R
 2_fit-model.R
```