<properties
pageTitle="IP Hardcoded"
description="Network Adapters"
infoBubbleText="A static IP has been set at the NIC level inside the guest OS preventing the RDP connectivity"
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
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>


# Static IP is set at the guest OS level
<!--issueDescription-->
A static IP has been set at the NIC level inside the guest OS preventing the RDP connectivity. 
<!--/issueDescription-->

Setting a Static IP at the guest OS level is not recommended for Azure VMs not using the multiple IPs per NIC feature. To restore the connectivity, assign a new static IP at the NIC level from portal. 

Virtual Machine [screenshot](https://docs.microsoft.com/azure/virtual-machines/windows/boot-diagnostics) will show that OS is fully loaded and waiting for the credentials.

## **Recommended Steps**

1.	In Azure portal, browse to [Network Interface](https://ms.portal.azure.com/#blade/HubsExtension/Resources/resourceType/Microsoft.Network%2Fnetworkinterfaces) attached to the virtual machine
2.	Select IP configuration and select the IP
3.	If the Private IP assignment is not Static, change it to Static.
4.	Change the IP address to another IP address that is available in the Subnet that you never used before
5.	Click Save on the top left and the virtual machine will restart to initialize the new NIC to the system
6.	Try connecting to the VM via RDP to validate that the connectivity has been restored.

In case you would like to use the old IP again, you must delete the old NICs in the guest to avoid the potential problem:

1.	Open Device Manager
2.	Select View > Show hidden devices
3.	Select Network Adapters
4.	Check for the adapters named as "Microsoft Hyper-V Network Adapter"
5.	You might see an unavailable adapter that is grayed out. Right-click the adapter and then select Uninstall
6.	Now all unavailable adapter should be cleared out from your system
