
![enter image description here](https://musingsofashibe.files.wordpress.com/2015/10/mrrobotlogo.jpg)
  
#The completion of EndorAB_DC1 31/10/2016

I manage to complete the last part of my  assignment fot the endorAB_DC1 AD.  
According to assignment i had to:  
 - create 3 template accounts.
 - Give privileges to the template accounts for the relative groups.
 - To create a home directory for each user that i have in EndorAB_DC1.
 - To make sure that Igor will not have access to Economy folder.
 - To insert the new users with their privilleges from page one, and to make sure that they will have Home directory too.  
  
For two of those actions it would be a good idea to have a bit of documentation, the issue with Igor and the matter with the home directories.  
  
The issue with Igor was not something difficult. I just had to evoke the privilleges from the "Ekonomi" folder. I did that in the properties of the folder to the tab of safety, on the advance options.  
  
The issue with home directories was complicated and i had to ask for help from the teacher. That was so complicated for two reasons, first because i was not able to understand what e were talking about. That the home directories are personal folders that are assigned for each user in order to be able the user to have his personal files. Second thing was that the creation of this folders and the assignment to the respective user had to be on the best way possible and according to some specifications:  
 - The creation of the home folders must to be first, it had to be manual, (no automated way for that). and i decided that the folders will have the same name with the username of the user that they are assigned to. On this point i should mention that for a moment I had a trouble to follow up with the naming characters of the folders. The NO SPACETAB was the reason that i decided that to name the folders according to the username was the most optimal idea.  
 - The other thing was that i tried to automatize the procedure by using saving the "\\EndorAB_DC1\homefolders\%UserName%" but that wasn't the case, as the automation is not recommended and is not available only through, (possibly), a powershell script or something, but as i said, automation is not recommended. I inserted the paths on the properties of the users on the tab profile.
 - All the home folders had to be on the partition E of every users account. That was easy to accomplish as the option for the partition was next to the path options.
 - Last thing that i forgot the name of my server. I was pretty sure that i gave a different name to my server but i was wrong. It took me 5 mins to find the mistake because of stress.  
  
#the installation of the workstation WS8
 I installed the WS8 as virtual machine on my HyperV and I configured its ipv4 to the following adresses:
	 - ip 10.20.0.160
	 - subnet mask 255.255.255.0
	 - standard gateway 10.20.0.1
	 - DNS 10.20.0.159  
	   
On my process to install the WS8 i faced another problem. I tried to install the the virtual machine as generation 2 and that causes some problems, (i don't know the details about the problem right now but i can assume that it is some kind of incomparability with the virtual prefab OSs).  
  
After that, the installation the login, and the check of the functionality of the EndorAB_DC1 was without any problem. The mission was accomplished and the WS8 was unistalled.
   
#What i added to the Active Airectory EndorAB_DC1
- Users
	- Percy Nilegård
	- Elisa Andersson
	- Kurt Nilsson
	- Adam Svensson
	- Lotta Luvine
	- Kalle Oborne
	- Ada Adair
	- Erik Lallerstedt
	- Laura Mauritz
	- Greger Lindström
	- Kjell Hansson
	- Mille Smith
	- Britt Högstedt
	- Dan Hylten
	- and 3 template accounts.
- Groups
	- Global
		- VD
		- LedningsGruppen
		- Data Admin
		- Ekonomi
		- Sälj Malmö
		- Sälj Göteborg
		- Lager
		- Verkstad 
	- Local
		- Ledning
		- Ekonomi Malmö
		- Sälj
		- Malmö Lager
		- Malmö Verkstad
		- Malmö
		- Göteborg
		- Data
  
On the partition C of the VM, (EndorAB_WS2012R2_DC1) i added the following folders:
 - Ledning
 - Ekonomi
 - Sälj
 - Lager
 - Verkstad
 - Malmö
 - Göteborg
 - Data
   
 The members and the privileges were graded properly according to the assignment, but i am not able to document them because of their complexity.

#The documents of the assigment.
![page 1](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local/endor.local%20photos/endor%20uppgift%201.JPG)  
  
![page 2](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local/endor.local%20photos/endor%20uppgift%202.JPG)  
  
![page 3](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local/endor.local%20photos/endor%20uppgift%203.JPG)  
  
![page 4](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local/endor.local%20photos/endor%20uppgift%204.JPG)  
  
![page 5](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local/endor.local%20photos/endor%20uppgift%205.JPG)  
  
![page 6](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local/endor.local%20photos/endor%20uppgift%206.JPG)  
  
![page 7](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local/endor.local%20photos/endor%20uppgift%207.JPG)



> Written with [StackEdit](https://stackedit.io/).