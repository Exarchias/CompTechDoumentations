
![enter image description here](https://musingsofashibe.files.wordpress.com/2015/10/mrrobotlogo.jpg)
  
#The completion of EndorAB_DC2 18/11/2016

I manage to complete the last part of my  assignment for the endorAB_DC2 DM.  
According to assignment i had to:  
 - create 1 new domain controller (EndorAB_DC2).
 - Add new users and groups according to the instructions.
 - To create a loggonscript on a shared folder.
 - To add a .bat script statement that assigns automatically the user folder to the respective folder in the homefolders assigned with the partition letter H:
  
The action to create the new domain controller and to add the extra users and groups , (plus the correspondand privilleges), was straight forward and i do not need to explain forward, only to add that i made those changes according to the instructions.  
  
The issue with the script was something that took me bit more time and efford i solved the needs of the instructions by writting two statements to the **loggonscript.bat** on the EndorAB_DC2 after the C folder:
 > net use  h: \\endorAB_dc1\homefolders\%UserName%
 > Echo welcome %UserName%
 > Pause 
  

  
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