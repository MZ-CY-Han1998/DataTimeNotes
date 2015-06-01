##File Conversion and Prep for XCMS 

The following explains how to take .raw extensions from Water UPLC/MS runs and convert to a usable format for XCMS (mzXML). 

For Windows Users

1)	Check to see if you have the following requirements for Proteowizard. If not, download the following before attempting to download Proteowizard:
a)	MSVC 2008 SP1 (x86)
b)	.NET Framework 3.5 SP1 
c)	4.0 

2)	Download proteowizard at http://proteowizard.sourceforge.net/downloads.shtml 
Download Windows 64-bit installer if working on a 64-bit.
Download Windows installer if working on a 32-bit. 

***Note: When converting files from vendors (e.g. Waters), Proteowizard will only be compatible with Windows users. For Mac users, this process can be completed on the Windows Vista computer in the lab. However, once the whole conversion process is complete and you have uploaded the mzXML file to your HPCC account, delete the files (optional: after transferring mzXML files to external hard drive) from the Windows computer.***

3)	Go to windows start, find the proteowizard icon, click it and open MSconvert. 

4)	If you have not already done so at this point, you will need to transfer .raw files from the mass spec facility server to a directory of your preference on your windows computer. For users using the lab computer, I have created a directory with the file path: Computer -> Local Disk (:C) -> Proteowizard -> raw files.  

To transfer files, use Filezilla (download here: https://filezilla-project.org/download.php?show_all=1)

a)	In Filezilla enter the following: 
-	Host: rtsf-ms.bch.msu.edu
-	Username: msftp 
-	Password: Mass.spec1234
b)	Find your data by navigating through the following files: /G2-XS QTof/SHADE_LAB.PRO/Data. 
c)	Right click data files and select add files to queue. On the left side, specify where you want the files to be transferred to on your computer by navigating to the appropriate directory. Once all files have been placed in the que and the transfer destination is set, select the Transfer at the header and select process queue. 


5)	Return to the proteowizard MSconvert window and select Browse to locate the .raw files you would like to convert and add them to process window. Select mzXML under file format, select 64-bit or 32-bit depending on your Windows version (Lab in computer is 32-bit), write a desired path for the output and leave all other defaults the same. Do not add filters. Start conversion. 

6)	mzXML file is now compatible for XCMS. Transfer file from your computer to the HPCC either by: 

a)	Following Siobhan protocol under Datatime notes 
b)	Filezilla: 
In the top dialog boxes, enter:
•	(Host) hpcc.msu.edu
•	(Username) <your username>
•	(Password) <your password>
•	(Port) 22
Transfer in a similar manner as stated above. 
