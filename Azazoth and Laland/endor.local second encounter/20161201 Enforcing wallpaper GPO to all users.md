
![enter image description here](https://musingsofashibe.files.wordpress.com/2015/10/mrrobotlogo.jpg)
  
#Forcing a specific wallpaper to all user on endor.local 01/12/2016

The first thing that i decided to do in order to do was to enforce a wallpaper policy. The decision was great because I had to face a challenge in order to achieve that and now everything looks easy as a piece of cake.  
  
Before I say something else it is important to point out that i was prepared from the begining. I was fully aware what is a GPO and where is and how works GPO manager, also about how the group policies are ordered and how we access them.  
Unfortunatelly that wasn't enough.  
  
As I worked my way through the assignment i faced some unexpected problems:  
 - The fact the i am not a native swedish speaker lead me accidentally to a false trail.
 - In the middle of the panic, I faced an issue with the NTFS rights and the sharing rights of the wallpaper that I wanted to use. I was aware of the issue but because of the chaos, my efforts were slow and inefficient.
 - A very serious mistake that I did the whole time was that I did too many actions without testing fist if something works. There were no consequenses from this mistake of mine but the existence of this faulty implementation spoils my efforts, and it shouldn't be repeated in the future.
   
![enter image description here](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local%20second%20encounter/photos%20from%20the%20HyperV%20machines%20of%20endorAB%20aasignment/Wallpapers/sharedbackground.jpg)
   
**1)** I choose a wallpaper to enforce to the users of endor.local, (I decided that it sould be something funny), and after downloading it, i pasted it to a shared folder that is sourced on the desktop of EndorAB_DC1 and it was called "Ps script". I tried to enforce the group policie, (I choose the wrong one).  
  
**2)** As i tried to fix the problem I fixed the issues with the NTFS rights, (i gave access to the wallpaper to all the users of the domain endor.local). The problem was not fixed but my actions on the matter of NTFS rights were correct.

**3)** We fixed the pathe by renaming it by changing the name of the folder from "Ps Script", (\\endorAB_DC1\Ps Script), to "psScripts", (\\endorAB_DC1\psScript), a name without white space is much better for paths and file managment. This action was  a correct one but still not effect were detected.  
  
**4)** Finally I noticed that because of my low level of Swedish I choose a wrong group policy to update.  
On this point i have to explain something. the architecture of the GPO files is divided in two major categories: Users and Computers, (and many subcategories that are following those two). Part of my mistake is that I assumed that the wallpaper is something that belong to the computers category and that was the beginning of my problems. The managment of the desktop screen and the wallpaper policy belongs to the users category. After realising that I activated the right policy and the problem fixed.  
  
**PS** I did not checked my deactivated policies as deactivated but as not configured, because accordingly of how windows server works that was the best thing to do, (deactivate means that it will not allow this policy to be enforced and not configurated means the policy is just not active).
  
#the installation of the workstation WS8
 I installed the WS8 as virtual machine on my HyperV and I configured its ipv4 to the following adresses:
	 - ip 10.20.0.160
	 - subnet mask 255.255.255.0
	 - standard gateway 10.20.0.1
	 - DNS 10.20.0.159  
	   
I had to install again the WS8(B) again, because I deleted the previous Working station (WS8A).  
The installation the login, and the check of the functionality of the EndorAB_DC1 was without any problem. The mission was accomplished and the WS8 was unistalled.
   
#What i added to the active driectory Endor.local
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
	- Klas Malmberg
	- Björn Mellander
	- Olle Häskilainen
	- Harald Blåtand
	- Fajitas Unger
	- Steve Joung
	- Hasse Alfredsson
	- Eisa Paiite
	- Halvar Helland
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
		- Promotion
		- Finland 
	- Local
		- Ledning
		- Ekonomi Malmö
		- Sälj
		- Malmö Lager
		- Malmö Verkstad
		- Malmö
		- Göteborg
		- Data
		- Reklam
  
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