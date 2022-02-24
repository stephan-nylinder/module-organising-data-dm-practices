---
title: Introduction to data organization
teaching: 20
exercises: 10
questions:
- What is our data, and how do we keep it in order?

objectives:
- Understand what to consider for maintaining data organization strategies in a project
- Develop good practices for data storage, processing and documentation
- Understand what to consider when settling for a file structure
- How we take the future into account in everyday research 

keypoints:
- Good data organization is fundamental to any research project
- Endpoint perspective is important

---

[//]: # "[Provenance]: ../fig/storage/Provenance.jpg"
[//]: # "[life-cycle]: ../fig/storage/life-cycle.png"

> ## About this episode 
> The data that you collect, organise, prepare, and analyse to answer your research questions, and the documentation describing it, is the lifeblood of your research. However, doing so without a prior idea of structure and how data will be used or viewed in the future, by yourself or someone else, can cause the data to become difficult to understand, or even useless. Working structures will accumulate deviations and become more unorganised over time regardless of the care we take.

In this episode we will look at data organization from a data life cycle perspective. 


## Mentimeter exercise
Question: What measures do you take in order to avoid file chaos in your data organisation?
<!--- Y: add a solution so that stand-alone readers, not participating in course, can get some sort of verification on their thoughts -->

## The data life cycle

When we consider different aspects of data organization, we can benefit from considering the general data lifecycle.

[//]: # "[life-cycle]: ../fig/storage/life-cycle.png"

Throughout its lifecycle, data can, and will, be subject to many possible types of changes:

* Data will be created/accumulated/collected; 
* Data cleaning procedures may be implemented;
* Errors are often found and corrected;
* New variables may be constructed;
* New information may be added from external sources;
* File formats may be changed;
* New data may be included;
* The data file structure may be changed for the purpose of increasing operability, etc.;
* Long term storage may require additional documentation

There are also possible types of changes to the data structure itself:

* New sub-projects can be initiated, or data splits may occur;
* Data files may be re-structured and/or re-organized into new folders;
* Collaborations can require certain data, but not all, to be stored in separate locations.


## Overview of data

Generation, processing, and analysis of data inevitably result in a number of edits in the data files and file structure. However, it is necessary to preserve the authenticity of the original research information contained in the data throughout the entire data lifecycle. At the same time we try to maintain our intended file structure. To develop a strategy for data management in a project you need to combine the project plan for data treatment with an overview of the data and documents your research will generate. The best time for planning is at the project startup phase, and a list of organisational considerations can consist of, but not be limited to:

* Initial and/or intended folder structure
* Which data files to cluster
* File naming convention
* Standards for dates/measures
* Documentation procedures

Preparing your project for receiving data and files should be a core aim in your research management, and should be documented in a data management plan (DMP). 

Sometimes a project will increase in size and scope, sub-projects will form, and data production will expand as new data are required and generated. When this happens, it may require changes and adaptations to already existant file structures. A file structure should be treated as a living document, continuously adapting to changes. File structures are not intended to remain in a static state throughout the data life cycle. 


### Whom are we organizing the data for?
Humans are an organizing species. We all recognize the benefits from keeping things in order, having an overview, and knowing where things are. It helps us being efficient in what we do, and brings a sense of relief and security not having to search for things we need. However, we also have individual measures and standards for interpreting the quality of data organization. What makes sense to me may be illogical to someone else, and vice versa.

In research we need to consider data organization from both the individual researchers perspective as well as from the research community perspective. As individuals, we want to organize a file system so that it makes sense to us. After all, we are the ones that will work with the data on a daily basis. At the same time we may be part of a larger group where data is shared among several researchers. Even further, the data endpoint is not the individual, the group, or even present day, but unknown researchers reusing our data in a yet-to-be future. 

Thus, we need to settle for a file structure and data organization process that works for us in both the short and long term, while also being viable in the future. 

<!--- Y: the section above (whom) and the section below (third-person) are overlapping, consider merging and reducing -->

## The third-person view
When settling for a data and file structure we need to take into account more than our own personal preferences. The ultimate goal for research data is making it FAIR, thereby increasing its usefulness for the scientific society of today and tomorrow. Data can, should, and will, be important to more researchers than ourselves. It should therefore be prepared and treated in such a way that it can be read and interpreted by others, as well as adapted for indexing in a data repository. This may come in conflict with our everyday use of the data. The data and file structure we find most convenient for ourselves, here, today, may not be the most convenient structure for our future selves, other researchers in general, or from a long term storage perspective.

Maintaining a file system adaptable to our own changing research requirements, while also being generally understandable tomorrow, can be a challenging task. We need to consider the present as well as tomorrow, and our own view as well as others.

### Reducing disorder
The perfect file system does not exist. No matter the intention or effort, all file systems tend to accumulate disorder over time. Good file system management is better focused on practices decreasing the level of disorder than eliminating it completely. Managing a file system does not by necessity require a lot of time. By selecting a manageable interval for file system maintenance we can optimize effort vs. gain. Regular scheduled maintenance over a project life span can achieve more and require less time in total, than a single effort when the project is in an end phase.

Having a well defined idea of our intended file system prior to beginning data collection can have substantial impact on the time required for file system maintenance later in a project. Starting data collection without such an idea can require a major effort by the time the project ends. 

<!--- Bilder på disorder vs. time --->

## Exercise 1
Rank the following data organization steps from 1-5 (1 being the one you believe you (will) spend most time doing, and 5 the least). Also mark with an "X" the steps you have implemented in your own research. 

- File naming convention
- Folder naming convention
- File versioning system
- File organisation documentation (README.txt)
- File and folder maintenance (moving, deleting)

<!--- Y: I misinterpreted the exercise, thought it was about what I think is most important, not most time-consuming... I suggest emphasizing 'spend most time' with italics or bold in case others misinterpret aw well 

Also, add a solution, so those not participating in course get some feedback --->

## Preserving file/data timelines

As data and files are created and used, they tend to split in different versions. Reasons may include modifying the contents of files, adding and/or subtracting data, or creating versions for trying different kinds of analyses or analysis setups. Versions tend to accumulate over time, and without an explicit strategy may eventually make file structure overview difficult or even impossible. We can take measures to decrease such disorder:

- A coherent file naming strategy. 
    By avoiding non-hierarchical file names (file.txt, file_new.txt, file_newer.txt, file_try.txt, file_add.txt etc.) we can circumvent having to re-interpret file chronology in the future. This is of particular importance when we publish data. There should never be confusion over which file was e.g. the published version. One way to prevent this is to version files.

- File versioning
    An easy-to-track and widely used way to document file history is to do file versioning (file_1.0.txt, file_1.1.txt, file.2.0.txt, etc.), where each new version of the file receives a new version number. Coupled with a separate document, or registration system, where each version is explained, anyone will be able to track changes through time.

<!---
## Exercise 2
 
## Exercise on filename interpretability?
Add exercise --->

<!--- Y: the examples above seems to span the whole module? If so, consider either dividing the bullets to the page they belong, or put this section on last (104) page --->
>> ### Examples of practices
>> Some best practice rules (UK Data Service, 2017a; Krejčí, 2014) can be summarised as follows:
>> - Establish the terms and conditions of data use and make them known to team members and other users;
>> - Create a ‘master file’ and take measures to preserve its authenticity, i.e. place it in an adequate location and define access rights and responsibilities – who is authorised to make what kind of changes;
>> - Distinguish between versions shared by researchers and working versions of individuals;
>> - Decide how many versions of a file to keep, which versions to keep (e.g. major versions rather than minor versions (keep version 02-00 but not 02-01)), for how long and how to organise versions;
>> - Introduce clear and systematic naming of data file versions and editions;
>> - Record relationships between items where needed, for example between code and the data file it is run against, between data file and related documentation or metadata or between multiple files;
>> - Document which changes were made in any version;
>> - Keep original (raw) versions of data files, or keep documentation that allows the reconstruction of original files;
>> - Track the location of files if they are stored in a variety of locations;
>> - Regularly synchronise files in different locations, such as using MS SyncToy (2016).
> {: .solution}
{: .discussion}


#
{: .callout}

{% include links.md %}