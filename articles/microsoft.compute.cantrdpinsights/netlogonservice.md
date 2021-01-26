<properties
  pageTitle="Netlogon service Not running"
  description="NetlogonNotRunning"
  infoBubbleText="Netlogon service is not running in your VM preventing network connectivity. See details on the right."
  service="microsoft.compute"
  resource="virtualmachines"
  authors="timbasham"
  ms.author="tibasham"
  displayOrder=""
  articleId="NetlogonService"
  diagnosticScenario="Netlogon service Not running"
  selfHelpType="diagnostics"
  supportTopicIds="32411835"
  resourceTags="windows"
  productPesIds="14749"
  cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Netlogon Service is not running

<!--issueDescription-->
We have investigated and identified that the Netlogon service is not running on this virtual machine <!--$vmname-->[vmname]<!--/$vmname-->, causing a loss of network connectivity. This could happen if the service is disabled accidentally or if the service is crashing or hung.

<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue please follow the steps in the [Netlogon not starting](https://docs.microsoft.com/troubleshoot/azure/virtual-machines/azure-vm-netlogon-not-starting) troubleshooting guide.
