<properties
pageTitle="VM Health Signal"
description="Network Adapters"
infoBubbleText="IP Properties"
service="microsoft.compute"
resource="virtualmachines"
authors="manavis"
displayOrder=""
articleId="vmhealthsignal_6a64eeb8-eb00-4d88-a24e-e577533724b9"
diagnosticScenario="IP Properties Error"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public"
/>


# Static IP is set at the guest OS level
<!--issueDescription-->
The virtual machine seems to have disabled DHCP and IP address not equal to null. This indicates static IP is set at the Guest OS level.
<!--/issueDescription-->

## **Customer Ready RCA**

You cannot connect to Microsoft Azure Windows Virtual Machine (VM) after you disable the default Network Interface (NIC) or manually set a static IP for the NIC.

Virtual Machine [screenshot](https://docs.microsoft.com/azure/virtual-machines/windows/boot-diagnostics) will show that OS is fully loaded and waiting for the credentials. In order to regain access to the VM please go through the following steps:

1.	In Azure portal, go to [Network Interface](https://ms.portal.azure.com/#blade/HubsExtension/Resources/resourceType/Microsoft.Network%2Fnetworkinterfaces) attached to the virtual machine
2.	Select IP configuration and select the IP
3.	If the Private IP assignment is not Static, change it to Static.
4.	Change the IP address to another IP address that is available in the Subnet that you never used before
5.	Click Save on the top left and the virtual machine will restart to initialize the new NIC to the system
6.	Try to RDP to your machine and it should be working now

After all of this, if you would like to use the old IP again, you must delete the old NICs to avoid the potential problem:

1.	Open Device Manager
2.	Select View > Show hidden devices
3.	Select Network Adapters
4.	Check for the adapters named as "Microsoft Hyper-V Network Adapter"
5.	You might see an unavailable adapter that is grayed out. Right-click the adapter and then select Uninstall
6.	Now all unavailable adapter should be cleared out from your system
