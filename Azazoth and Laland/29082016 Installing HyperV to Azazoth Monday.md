
![enter image description here](https://musingsofashibe.files.wordpress.com/2015/10/mrrobotlogo.jpg)
  
#Installing HyperV to Azazoth Monday 29/08/2016
  
Azazoth is the new  computer that replaced Exarchos. Azazoth is actually a server, configurated as server and with windows server 2012 installed as OS.

My first non-trivial task that i had to do to Azazoth it was to prepare it for a virtual network in the form of Domain.
The very first part of it was to install the hyperV feature.
This process is separated in two parts:
-the preparation of the Administrator account for reasons of safety and functionality, and
-the installation of HyperV  
  
##The preparation of the Administrator@Azazoth
Before any serious server task on Azazoth, i had to ensure that the administrator@azazoth was ready according to safety and functionality measures. That means:
-i had to use a strong password. Obviously, (even if we talk for a small lokal, and highly experimental virtual network) i can't share my password here, but my password applies to all the safety standards. As bonus action i took the necessary  procautions to provide any ambitious hacker with the necessary amount of trolling.  
-I had to configure a static ip for my Server machine. i did that by register the 4 ipv4 adresses to my name(10.20.0.158 - 10.20.0.162) and to assign the 10.20.0.158 as the ipv4 of my Server machine (Azazoth). For standard gateway and DNS i used the 10.20.0.1 as it is recommended, but before i configure azazoth as domain controller  i will change those, probably i will assign the same adress with Azazoth's as my standard gateway, and i will assign the return ipv4 adress (127.0.0.1) as my DNS. I say probably because i am not sure and changes are to be expected. the only sure thing is that i am not willing to embarass my self by dropping the internet connection for the whole class.
To drop the connection for the whole class it could be fun, but nahh... at least not in my assignment.
-I had to provide to my precious self the luxury of an problemless envirovment, (Hakuna Matata!), so i decided that it was a great idea to deactivate IE advance security feature, and the firewall for local destinations.

![enter image description here](https://i.ytimg.com/vi/TErp_BjM2Cc/maxresdefault.jpg)

##The istallation of HyperV
Ok, in this one i will be honest. the truth is that i used ready instractions for the whole of the process. Of course i didn't anything blindly, (i had the full control of what i was doing), but neithertheless i followed instructions and it is better approach to share them here instead of transform them to my instructions:

###Install Hyper-V and create a virtual machine

Updated: June 6, 2016
Applies To: Windows 8, Windows 8.1, Windows Server 2012, Windows Server 2012 R2  
Learn how to get started with Hyper-V on Windows Server 2012, Windows Server 2012 R2, Windows 8, or Windows 8.1    Professional and Enterprise editions. To learn more about Hyper-V including system requirements, see Hyper-V overview. For the most current version of this topic, see Install Hyper-V on Windows 10 or Install the Hyper-V role on Windows Server 2016.  
In this document  

####Prerequisites
- Step 1: Install Hyper-V
- Step 2: Create a virtual machine
- Step 3: Install the guest operating system
- Step 4: Install or upgrade integration services  

###Prerequisites
Before you install Hyper-V, make sure that you have the following:  
A user account with administrator permissions for the computer.
Enough memory to run all the virtual machines that you plan to run at the same time.  
Software to install as the guest operating system for the virtual machine.  
 
###Step 1: Install Hyper-V
Install Hyper-V so you can create and run virtual machines on this computer.  
You can install the Hyper-V role in Server Manager or by using Windows PowerShell.  
####Install the Hyper-V role by using Server Manager
- In Server Manager, on the Manage menu, click Add Roles and Features.
- On the Before you begin page, verify that your destination server and network environment are prepared for the role and feature you want to install. Click Next.
- On the Select installation type page, select Role-based or feature-based installation and then click Next.
- On the Select destination server page, select a server from the server pool and then click Next.
- On the Select server roles page, select Hyper-V.
- To add the tools that you use to create and manage virtual machines, click Add Features. On the Features page, click Next.
- On the Create Virtual Switches page, Virtual Machine Migration page, and Default Stores page, select the appropriate options.
- On the Confirm installation selections page, select Restart the destination server automatically if required, and then click Install.
- When installation is finished, verify that Hyper-V installed correctly. Open the All Servers page in Server Manager, select a server on which you installed Hyper-V. Check the Roles and Features tile on the page for the selected server.
  
[For more information about the instructions click here](https://technet.microsoft.com/en-us/library/hh846766%28v=ws.11%29.aspx)  
> Written with [StackEdit](https://stackedit.io/).