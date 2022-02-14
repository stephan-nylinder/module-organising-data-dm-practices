---
title: Data preservation
teaching: 10
exercises: 10
questions:
- What can we do to maintain data integrity and authenticity?
objectives:
- Incresing file findability
- File naming concepts
- 

keypoints:
- Endpoint perspective is important
- Be careful not to settle for a too rigid file system
---

> ## About this episode 
> Research data can be organized in nearly an infinite number of different ways. When settling for a system we need to consider our own preferences, the ones we share project or data with, and how data will be preserved and reused in the future. We also need to consider that all file systems will accumulate disorder over time, and what measures we can take in order to make sure the level of disorder becomes a problem. 


# Plan a storage strategy
It is an important aspect of your data management planning to determine what your storage needs are and select solutions accordingly. Factors that play a role are, for example, data sensitivity, ease of access, file size and overall data volume. You can also ask yourself where, how and by whom your data will be produced, accessed, transformed, and transferred throughout and beyond the project.

![Data life cycle][life-cycle]

One way of categorising different types of storage options is:
* Portable devices – Laptops, tablets, external hard-drives, flash drives and Compact Discs
* Cloud storage - E.g. Google Drive, OneDrive, Dropbox, a University’s OwnCloud, Open Science Framework and Tresorit
* Local storage – Desktop computers and personal laptops
* Networked drives – Shared drives on university servers, NAS servers (Network Attached Storage) or infrastructures (such as SNIC)

> ### Discussion
> What storage categories do you use and what factors do you consider when selecting which category to use or not to use? 
> * Portable devices – Laptops, tablets, external hard-drives, flash drives and Compact Discs
> * Cloud storage - E.g. Google Drive, OneDrive, Dropbox, a University’s OwnCloud, Open Science Framework and Tresorit
> * Local storage – Desktop computers and personal laptops
> * Networked drives – Shared drives on university servers, NAS servers (Network Attached Storage) or infrastructures (such as SNIC)
>
>> ### Portable devices
>> - Do: use for temporary, short-term storage for non-sensitive data, e.g. in the field or to transport data and files when online transmission is not possible.
>> - Do: use in combination with encryption and strong password protection, especially if working with sensitive information (see 'Security').
>> - Do: conduct regular checks to ensure your device is working and that files are accessible.
>> - Do not: use for long-term storage or master copies of your data and files.
> {: .solution}
>
>> ### Cloud storage
>> - Do: use cloud services for granting shared, remote and easy access to data and other files to all involved in the project.
>> - Do: Read the terms of service. Especially focus on rights to use content given to the service provider.
>> - Do: Opt for European, national, or institutional cloud services which store data in Europe if possible.
>> - Do not: make this your only storage and backup solution.
>> - Do not: use for unencrypted (sensitive) personal data.
> {: .solution}
>
>> ### Local storage
>> Using desktop computers and personal laptops as the primary way of storing and accessing data and files is only suitable for projects involving very few people (ideally: only yourself) and where data and files will not have to be moved back and forth between personal computers frequently.
>> 
>> If you plan to work on the data on different (local) workstations, e.g. with your laptop at home and the desktop in the office:
>> - Do: make sure that you always work on the most current version of your files, for example with the help of versioning software or version control guidelines (see 'Data authenticity, versions and editions').
>> - Do: make sure that the most current version is always backed up (see 'Backup').
> {: .solution}
>
>> ### Networked drives
>> - Do: Use for distributed collaborative projects involving many people who need access to data and files
>> - Do: use in combination with a suitable security strategy to protect data and files against unauthorised access (see 'Security').
>> - Do: use in combination with strict versioning rules (see 'Data authenticity, versions and editions')
>> - Do: think about long-term archival solutions for data that is complete and has been analysed. Valuable storage space might be released in this way.
>> - Do: work with rights and permissions to ensure that not everyone has access to everything if this is not required (e.g. make access to master files more restricted than access to working files).
> {: .solution}
>
{: .discussion}

## Plan a backup and disaster recovery strategy
A backup strategy in one sentence would be: Make at least three backup copies of the data on at least two different types of storage media, keep storage devices in separate locations with at least one off-site, regularly check whether they work, ensure you know the process and follow it. 

> ### Discussion
> What are examples of potential causes for data loss in a research project?
>
>> ### Examples
>> - Hardware failure;
>> - Software malfunction;
>> - Malware or hacking;
>> - Human error (research data accidentally gets deleted or overwritten or is lost in transport);
>> - Theft, natural disaster or fire;
>> - Degradation of storage media.
> {: .solution}
>
{: .discussion}


> ### Creating a backup strategy in 10 steps
> 
> 1. Find out whether your institution has a backup strategy
> 2. Determine what you want to back up
> 3. Decide how many backups you will need and how frequently to back up
> 4. Decide where backups will be stored
> 5. Determine how much storage capacity will be needed
> 6. Determine if there are tools you could use to automate backup
> 7. Determine how long backups will be kept and how they will be destroyed
> 8. Determine how personal data will be protected
> 9. Devise a disaster recovery plan
> 10. Assign responsibilities 
{: .callout}

> ### Further reading
>
> - [ELIXIR (2021) Data storage. In Research Data Management Kit. A deliverable from the EU-funded ELIXIR-CONVERGE project (grant agreement 871075).](https://rdmkit.elixir-europe.org/storage.html)
> - [--- (2021) Processing. In Research Data Management Kit. A deliverable from the EU-funded ELIXIR-CONVERGE project (grant agreement 871075).](https://rdmkit.elixir-europe.org/processing)
> - [--- (2021) Data analysis. In Research Data Management Kit. A deliverable from the EU-funded ELIXIR-CONVERGE project (grant agreement 871075).](https://rdmkit.elixir-europe.org/data_analysis.html)
>