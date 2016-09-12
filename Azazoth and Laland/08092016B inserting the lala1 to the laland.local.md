
![enter image description here](https://musingsofashibe.files.wordpress.com/2015/10/mrrobotlogo.jpg)
  

#Addition of lala1.laland.local to the laland.local domain Thursday 01/09/2016

This documentation describes briefly the process of adding the pc lala1(yet lala1.laland.local) to the domain laland.local.
I followed the typica instructions and i added the lala1.laland.local through itself to the domain.  
  
As it is expected the lala1.laland.local is a windows 7 professional pc. Windows 7 professional are necessary to insert the pc to the domain. I need to say though again that a domain controller is necessary to regulate the domain and it has to be a windows server. Anyway as i said the istallation of the lala1.laland.local is made through the lala1.laland.local as i changed lala1.laland.local from a local pc who belong to a homegroup to a member of a domain.  
  
##Few details:
- Domain controller for laland.local is the azazoth.laland.local who has two members, administrator@azazoth.laland.local, (as usually) and exarchias@azazoth.laland.local
- Lala1.laland.local has one user admin@lala1.laland.local, and its ipv4 is congured as follows
	- ipv4 is 10.20.0.159
	- submask 255.255.255.0
	- standard gateway 10.20.0.1 (to the router ALWAYS)
	- and  DNS server the domain controller 10.20.0.158 (for standard forwarding). I took confirmation by the teacher that my ipv4 configurations is correct. so i will keep this tactic for now.


> Written with [StackEdit](https://stackedit.io/).