
![enter image description here](https://musingsofashibe.files.wordpress.com/2015/10/mrrobotlogo.jpg)
  
#Difficulties in order to activate the virtual machine of the EndorAB_WS2012R2_DC1 27/10/2016

My plan to activate the first of the two virtual machines that will host the endorAB_WS2012R2_DC1 wasn't without problems. Even if the HyperV was properly installed, a problem with the RAM was enough to cause a trouble. Actually a small hardware failure, (as i assume, i am not sure), caused the failure of 4,5Gb from 8Gb of the RAM that has as result the ability for my computer to use only the 3,5Gb of the RAM. That means that my server computer was not able to work any VM because the lack of RAM.  
  
![enter image description here](![enter image description here](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local%20second%20encounter/photos%20from%20the%20HyperV%20machines%20of%20endorAB%20aasignment/endorAB_WS2012R2_DC1/27%20and%2028%20October%202016/1.JPG)
  
The problem finally solved by adjusting again the RAM cards to their sockets, (as I assume, i wasn't able to see properly, but it was some kind of adjustment  to the Hardware)  
  
![enter image description here](![enter image description here](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local%20second%20encounter/photos%20from%20the%20HyperV%20machines%20of%20endorAB%20aasignment/endorAB_WS2012R2_DC1/27%20and%2028%20October%202016/3.JPG)  
  
There was and another issue that didn't let me to activate the virtual machine and this time because of the lack of some kind of "tool". the problem solved through BIOS but i wasn't able to document the details of the solution.  
  
After that i was able to install the Virtual Machine on the partition "D:\HyperV VMs\VMs". i decided instead of using physical copy of Windows Server 2012 R2, to finally use ISO file. This decision was not voluntarily but i was forced to do so because i wasn't able to access the physical DVD driver through the virtual machine.   
  
![enter image description here](![enter image description here](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local%20second%20encounter/photos%20from%20the%20HyperV%20machines%20of%20endorAB%20aasignment/endorAB_WS2012R2_DC1/27%20and%2028%20October%202016/7.JPG)
  
#the installation of the Windows Server 2012 r2 to the EndorAB_WS2012R2_DC1 and the first chunk of data 28/10/2016
 I installed wibndows server 2012 r2 to my machine VM (EndorAB_WS2012R2_DC1) and I configured its ipv4 to the following adresses:
	 - ip 10.20.0.159
	 - subnet mask 255.255.255.0
	 - standard gateway 10.20.0.1
	 - DNS 127.0.0.1  
	 
 As i did one more time I faced unfortunately a small problem because i forgot again to install the DNS role so i wasn't able to connect to internet, (i fixed that quickly).  
  
At this point i have to say that i faced and one other small, (i hope), issue that i decided that for the moment it wasn't worth the trouble to fix it. As the Server administrator started there we 3 persistence warnings on local server and other servers, but i hadn't the energy to try to solve them.  
  
![enter image description here](![enter image description here](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local%20second%20encounter/photos%20from%20the%20HyperV%20machines%20of%20endorAB%20aasignment/endorAB_WS2012R2_DC1/27%20and%2028%20October%202016/8.JPG)

The installation of the Active directory was carefree and i gave to the Active Directory the name endorAB_DC1
  
#Starting with the assignment 28/10/2016
This time to start with the assignment was much easier from the last time because i knew the process.  
##What i added to the Active Airectory EndorAB_DC1
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