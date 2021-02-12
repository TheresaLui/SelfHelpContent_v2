<properties
pageTitle="NSI service Not running"
description="NSINotRunning"
infoBubbleText="Network Store Interface Service (NSI) is not running in your VM preventing network connectivity. See details on the right."
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani,timbasham"
ms.author="tibasham"
displayOrder=""
articleId="NSIService"
diagnosticScenario="NSI service Not running"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Network Store Interface (NSI) Service is not running

<!--issueDescription-->
The NSI service is not running on the virtual machine <!--$vmname-->[vmname]<!--/$vmname-->, causing a loss of network connectivity. This could happen if the service is disabled accidentally or if the service is crashing or hung.
<!--/issueDescription-->

## **Recommended Steps**

To resolve the issue, follow the steps in the [Network Store Interface service not starting](https://docs.microsoft.com/troubleshoot/azure/virtual-machines/azure-vm-nsi-not-starting) troubleshooting guide.
