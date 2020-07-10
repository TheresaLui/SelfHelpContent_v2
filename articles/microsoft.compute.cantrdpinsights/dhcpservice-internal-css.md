<properties
pageTitle="DHCP not running"
description="DHCP Service not running"
infoBubbleText="DHCP Service not running on your VM preventing network connectivity"
service="microsoft.compute"
resource="virtualmachines"
authors="manavis"
displayOrder=""
articleId="vmhealthsignal_f149f2b5-881f-4d4b-8e41-4b428e9e822d"
diagnosticScenario="DHCP Service not running"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# DHCP Client service is not running
<!--issueDescription-->
The DHCP service is not running on the Virtual Machine. This service registers and updates IP addresses and DNS records for this computer. If this service is stopped, this VM will not receive dynamic IP addresses and DNS updates. If this service is disabled, any services that explicitly depend on it will fail to start.
<!--/issueDescription-->

## **Recommended Steps**
To mitigate the issue please try the below steps from [Serial Console](https://docs.microsoft.com/azure/virtual-machines/windows/serial-console)
  * Query the state of the service by executing `sc query DHCP`
  * If the service is stopped, try starting the service by executing `sc start DHCP`
  * If the service is hung with a status starting or stopping, try to stop the service `sc stop DHCP` and start it again using `sc start DHCP`
  * Once the service is started, set the service startup type to automatic by executing `sc config DHCP start= auto`

In case the service is not starting due to an error or due to an issue with the depending processes, a memory dump needs to be collected to investigate further. So please reach out to us approving the memory dump collection.
