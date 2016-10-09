
![enter image description here](https://musingsofashibe.files.wordpress.com/2015/10/mrrobotlogo.jpg)
  
#Creating endor.local 19/09/2016

On Monday 19/09/2016 i started the process to install a new active domain directory that will be in the domain endor.local and it will have computer, users, and OU according to the instractions, and it has to be copied on a hyperV virtual domain, (i will return to this part when the time will come later... the instructions are bit unclear. )  
  
The task that i had on hand on monday was:  

##To change the domain from laland.local to endor.local

I learned on the hard way that is not possible to have to diferent AD to windows server 2012 R2 without to use hyperV, so in order to be able to avoid sensless use of hyperv i decided to remove my previous Active directory domain laland.local and to add in its place the brand new endor.local.  

##To add some shit inside
Actually the instructions are a list with needs to be added in a bit chaotic order that can lead to mistakes, (i believe that was in purpose to add bit challenge to the assignment).  

##What i have finally done
I have done the following structure.  
###endor.local
- Users
- Groups
	- Admin 
	- Data
	- Ekonomi
	- Göteborg
	- Lager
	- Ledning
	- Malmö
	- Sälj
	- Verkstad  
  
And i will continue to adding more stuff always according to the instructions, (probably i will upload photos about that but for now i am done).  

#The documents of the assigment.
![page 1](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local/endor.local%20photos/endor%20uppgift%201.JPG)  
  
![page 2](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local/endor.local%20photos/endor%20uppgift%202.JPG)  
  
![page 3](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local/endor.local%20photos/endor%20uppgift%203.JPG)  
  
![page 4](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local/endor.local%20photos/endor%20uppgift%204.JPG)  
  
![page 5](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local/endor.local%20photos/endor%20uppgift%205.JPG)  
  
![page 6](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local/endor.local%20photos/endor%20uppgift%206.JPG)  
  
![page 7](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Azazoth%20and%20Laland/endor.local/endor.local%20photos/endor%20uppgift%207.JPG)



> Written with [StackEdit](https://stackedit.io/).