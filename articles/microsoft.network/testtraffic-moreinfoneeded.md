<properties
pageTitle="More information is needed"
description="More information is needed to run the diagnostic"
infoBubbleText= "More information is needed to run the diagnostic"
service="microsoft.network"
resource="virtualnetworks"
authors="spacest"
ms.author="Mario.Liu"
displayOrder=""
articleId="TestTrafficNeedMoreInfo"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="CloudNet_VirtualNetwork"
/>

# More information is needed to run the Troubleshooter

<!--issueDescription-->
The VM Connectivity Troubleshooter could not run successfully because the required information is missing. All the three selections (virtual machine, traffic direction, and port number) need to be filled to run the troubleshooter. 
<!--/issueDescription-->

## **Recommended Steps**

1.	Select the virtual machine. You will see a list of virtual machine(s) in the virtual network you’re having issue with. If you don’t see any, that means there’s no virtual machine in the virtual network you selected before. Please go back and select a different virtual network.
2.	Select the traffic direction. It’s either from VM to Internet, or from Internet to VM.
3.	Select the port number. For now, you can only pick one of the most used port numbers at a time. More will be added with the improvement of this troubleshooter.
4.	Click Submit again.

**Note**: If “Other, don’t know or not applicable” is selected, the troubleshooter won’t detect the issue. 
