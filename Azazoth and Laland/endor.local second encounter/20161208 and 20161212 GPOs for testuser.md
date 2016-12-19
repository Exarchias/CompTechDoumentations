
![enter image description here](https://musingsofashibe.files.wordpress.com/2015/10/mrrobotlogo.jpg)
  
#Creating the testuser and adding a GPO for testuser on endor.local 08/12/2016

According to the instructions i had to build a test user with the name "testuser" and password the same with the other users on the network (a default password that I do not wish to write inside a documentation), and I did so:
 - I created the user testuser with the password.
 - I enforced few GPOs to the user for several issues for example a denied access to the control panel and all the applications of the control panel.
 - I had already managed to enforce a wallpaper policy as it is known trough my previous documentation.
 - And finally I had to block the access for the user to some pages. This part was the most difficult one, and the cries out my need to study bit more about DNS, (it seems easy but is not, it has deep and interesting theory behind it).  
  
##Educational notices for GPOs

It is always useful to know the structure in which the GPOs are stored, (the know-where makes the life of the administrator bit easier), but we can safely say that the GPO theory is easy. Everyone has just to remember two things:  
 - Every GPO has 3 stages. Active=when the policy is applied and active. Inactive=when the policy can't be activated and unassigned=when the policy is just not activated.
 - The GPO are separated in two large groups. The groups of GPOs that are applied for Computers, and those who are applied for users.
 - Every GPO is applied as file-right to one or many owners.
  
  
## The creation of the Testuser was te easy part.

About the creation of the testuser we don't have any secret. The testuser created according to the general instructions about user creations.  
The thing that is worthy to be mentioned is that I created a homefolder fo the testuser on the harddisc of the EndorAB_DC1.  

##The wallpaper was already enforced

As i said. I already did this in my previous step of my assignment, and I already wrote a detailed documentation about it. It was a tough process that helped me a lot with the NTFS rights and GPOs.
   
![The chosen wallpaper for all the users](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local%20second%20encounter/photos%20from%20the%20HyperV%20machines%20of%20endorAB%20aasignment/Wallpapers/sharedbackground.jpg)
   
##The most important GPO
I added many several GPOs for the testuser as tried to restict access to as many things as possible.
The main thing was the GPO for denial of access to the control panel.
This specific GPO if applied it can deny access to Control panel and to all the items of control panel recursively.
Not something difficult but it was worth a mention to the documentation.  

![The most important GPO](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local%20second%20encounter/photos%20from%20the%20HyperV%20machines%20of%20endorAB%20aasignment/endorAB_WS2012R2_DC1/08%20and%2012%20December/8_6.JPG)
  
##The denial of access to some specific pages
Ok... this was a difficult one and it deserves the most part of this documentation. The old GPO that it could deny access the access to some pages through the internet explorer applies only in older versions of Windows server (WS 2003 and earlier), so i had to fight my way through DNS options.  
The main issue with DNS is that is not that simple that it looks like and it needs further study, (at least in my case).  
the actions that i tried to do was a simple forwarding, and despite the fact that i knew where and the how two of forwarding I stumbled to some issues:
 - The type of the dns: there are many types of access, that are defining things like the priority and the extra roles that a DNS entry can have. I need to study this part more.
 - The difference between main DNS and the secondary DNS and the relations between them.
 - And... the syntax (no camelback syntax for the names of the every entry).
 - Last important thing is that we have to flush and restart the DNS after every change. That is obvious, but if ignored it can lead to problems.

![The restricted access to some web pages](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local%20second%20encounter/photos%20from%20the%20HyperV%20machines%20of%20endorAB%20aasignment/endorAB_WS2012R2_DC1/08%20and%2012%20December/12_1.JPG)
   
#What i added to the active driectory Endor.local
- Users
	- Testuser
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