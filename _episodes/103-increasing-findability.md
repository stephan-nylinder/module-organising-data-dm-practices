---
title: Increasing file findability
teaching: 10
exercises: 10
questions:
- What can we do to increase data findability?
objectives:
- Making files findable
- Associating files with metadata 

keypoints:
- File findability is connected to the future value of research
- Meta tagging files with relevant information increases findability

---

> ## About this episode 
> A key point in data management is finding information among large sets of files and data. Knowing all your files and their contents can be a manageable method in the short term, but as files and folders increase in size and numbers and old projects are replaced with new ones, finding specific information becomes harder. You might struggle to find files you know exist, or critical decisions are difficult to make due to information overload or a paralysing mass of irrelevant files/folders/data.
> 1. TOC
> {:toc}
> {: .toc}
{: .callout .toc}

## Why is file findability a problem?
When we think about findability we often make implicit analogies to search engines. Type in what you want to find in a specific application (e.g. web browser) and quickly obtain a list of search results. The problem with this analogy is that a web browser is used for finding information that was created with the purpose of being found! Working with research data requires us to think differently.

When we collect data and organise it for research purposes, findability is not necessarily our primary, or even a significant, motivation. 
 
### Multiple file copies
One way to increase findability is to make copies of files and store in process specific locations. A part of this process may even include renaming duplicated files in a way that suits the new context. The risks should be obvious to everyone. The same also applies to collaborations lacking common storage and working spaces. Files may be distributed among project participants by mail or portable devices (Flash drives, hard drives, etc.), creating situations where multiple copies exist simultaneously.
<br>

      **Pros**: Someone is (always?) guaranteed to have the latest version of a file!<br>
      **Cons**: Who has the latest version of a file?

While such a system may seem feasible, the amount of administration to keep track of distribution schemes and file edits will quickly outweigh the benefits.

Any system dependent on tracking the use of multiple file copies is strongly advised against! 
<br>

### File shortcuts
Shortcuts are an easy, feasible, and intuitive way to increase findability while avoiding file duplications. A shortcut can point to a file location anywhere, even on a network drive.
<br>

      **Pros**: Easy to create, file name of shortcut can be changed without compromising the original file integrity and may even increase findability when named differently.<br>
      **Cons**: Shortcut may break if original file location or name is changed. Easy to lose orientation if not maintained regularly.

### Metadata<br>
A good and informative file name is a great start, but there is a limit to how much information you can pack into a file name before the length itself becomes a problem. This is where metadata comes in. For the purpose of findability we can associate the file name with metadata stored elsewhere, for example in a text file kept together with the files.

> ### Example <!-- Exercise instead of Example? --> 
> 20220115_MyFile_Project1_Location_Dataiteration1_V1.xml<br>
> 20220115_MyFile_Project1_Location_Dataiteration2.xml<br>
> <!-- I think the file names could be a bit more specific (not MyFile eg), and add in the text a bit of context that one would want to capture. Reason is that I don't think anyone would reach the solution without taking a peak on it -->
> Write an example of metadata information explaining the above file names and the file contents, and descibe where and how to provide it.
>
>> ### Solution 
>> In file folder:  
>>                 
>>    20220115_MyFile_Project1_Location_Dataiteration1_V1.xml<br>
>>    20220115_MyFile_Project1_Location_Dataiteration2.xml<br>
>>    Metadata.txt<br>
>>```    
>>(Metadata.txt content)
>>
>>20220115_MyFile_Project1_Location_Dataiteration1_V1.xml 
>>First version of X data from Y, with additions of Z made by A and B on 20220110 including suggestions by C.
>>
>>20220115_MyFile_Project1_Location_Dataiteration2.xml
>>Contains X data from Y, with additions of Z made only by A on 20220111 not including suggestions by C.
>>```
>>Here the Metadata.txt lists the file name and associates it with additional data not possible to fit into the file name itself. By adding it separately and associating it with the file name we increase findability a lot.
> {: .solution}
{: .discussion}
<br>

## Keyword tagging
While metadata can be added separately it is first and foremost descriptive of the file contents. An extra layer to increase findability is by tagging the metadata with specific keywords. For files used in a specific context, but stored in separate locations, adding keywords will help tie the files together.

If possible use controlled vocabularies!

For the daily routine in working with data it all seems a bit over the top to combine file naming conventions with both metadata files and tagging, but your future self (and others) may be eternally grateful!<br>
``` 
(Metadata.txt content)

20220115_MyFile_Project1_Location_Dataiteration1_V1.xml 
First version of X data from Y, with additions of Z made by A and B on 20220110 including suggestions by C.
Keyword HumptyDumpty Genome_Assembly 

20220115_MyFile_Project1_Location_Dataiteration2.xml
Contains X data from Y, with additions of Z made only by A on 20220111 not including suggestions by C.
Keyword Published
```
<br>

## How to encode/extract metadata from filenames

Deliberately use "-" and "_" to allow recovery of meta-data from the filenames:

- "_" underscore is used to delimit units of meta-data to be used in searches.
- "-" hyphen is used to delimit words to increase readability<br> (Compare to an URL slug - www.scilifelab.se/this-is-a-slug).
<br>
<br>


```
| Bad |

myabstract.docx                                     
Joe’s Filenames Use Spaces and Punctuation.xlsx     
figure 1.png                                        
fig 2.png                                           
JW7d^(2sl@deletethisandyourcareerisoverWx2*.txt     


| Better |

2014-06-08_abstract-for-sla.docx
joes-filenames-are-getting-better.xlsx
fig01_scatterplot-talk-length-vs-interest.png
fig02_histogram-talk-attendance.png
1986-01-28_raw-data-from-challenger-o-rings.txt
```
<br>


> ## Exercise
> Download the [compressed example directory](../data/Example_project_begin.zip) and unzip the file on your laptop. The directory contains a collection of files from an imaginary project, somewhat resembling what the initial phase of a project can look like. Given the files provided:
>
> 1. Create a proper hierarchical folder system based on the file names and contents.
> 2. Rename files in a consistent manner if required, such that it reflects both contents and file version. Consider number and date formats as well.
> 3. Optionally, create a file for meta tagging files with keywords according to file contents.
> 
>> ### Example of outcome
>> 1. An example of a fully re-ordered directory can be downloaded [HERE](../data/Example_project_improved.zip) 
>> 2. A text format representation of an improved directory can be downloaded [HERE](../data/tree.txt) 
> {: .solution}
{: .discussion}
