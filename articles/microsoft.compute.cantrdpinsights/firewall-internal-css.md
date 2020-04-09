<properties
pageTitle="Firewall Not running"
description="Firewall Setting"
infoBubbleText="Windows firewall service is not running in your VM preventing connectivity.  See details on the right."
service="microsoft.compute"
resource="virtualmachines"
authors="timbasham"
ms.author="tibasham"
displayOrder=""
articleId="vmhealthsignal_16f84eeb-3655-45bb-a60d-2839f159fbf4"
diagnosticScenario="Firewall Misconfigured"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Windows Firewall is not running

<!--issueDescription-->
The Windows firewall service is not running in your virtual machine. The service must be running to enable network connectivity to the virtual machine.
<!--/issueDescription-->

## **Recommended Steps**
To resolve the issue, please try the steps below using the Azure virtual machine serial console tool.  If you’re unfamiliar with the serial console or would like additional information, please refer to our user [guide](https://docs.microsoft.com/azure/virtual-machines/windows/serial-console).
#### From the console: ####
  * Query the state of the service by executing `sc query Mpssvc`
  * If the service is stopped, try starting the service by executing `sc start Mpssvc`
  * If the service is hung with a status starting or stopping, try to stop the service `sc stop Mpssvc` and start it again using `sc start Mpssvc`
  * Once the service is started, set the service startup type to automatic by executing `sc config Mpssvc start= auto`

If the service is not starting due to an error or an issue with dependent processes, a memory dump needs to be collected to continue troubleshooting. 
