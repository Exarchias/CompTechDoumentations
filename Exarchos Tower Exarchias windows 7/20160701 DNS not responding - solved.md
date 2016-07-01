![alt text](https://raw.githubusercontent.com/Exarchiasghost/CompTechDoumentations/master/Exarchos%20Tower%20Exarchias%20windows%207/photos%20Exarchos/20160627%20DLink.JPG "D-link connected to exarchos")
    

**Date:** 01/07/2016  
**PC:** Exarchos  
**Operation:** resolving the issue with virtual network Jo3.Kristianstad  
**Operator:** Robert Alm  
**Issue:** Connection problem between switch and the router/server Jo3.Kristianstad, probably because of the switch. the Jo3.Krstianstad is visible but something seems to be wrong. We tried to solve that with changeng IP,  but it seems we were not able to touch anything to the configuations with safety. 
The problem finaly solved. As it seems my pc/switch connected to a virtual network after a problem that the network had by mistake of the operator that blow the internet connection off.   
**Resolve:** the issue is solved. We used the command ipconfig /release and ipconfig /renew through the cmd window.  
**SOS** It is a really great idea to map my network, in order to be able to solve issues like that bit easier.