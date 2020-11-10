<properties
  pageTitle="BFE Service"
  description="BFE Service not running"
  infoBubbleText="Base Filtering Engine Service (BFE) is not running which may prevent RDP connectivity."
  service="microsoft.compute"
  resource="virtualmachines"
  authors="timbasham"
  ms.author="tibasham"
  displayOrder=""
  articleId="vmhealthsignal_10f4f09d-a1e8-4536-b167-8d2573fb4f0a"
  diagnosticScenario="BFE Service"
  selfHelpType="diagnostics"
  supportTopicIds="32411835"
  resourceTags="windows"
  productPesIds="14749"
  cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>


# Base Filtering Engine (BFE) Service is not running
<!--issueDescription-->
The Base Filtering Service (BFE) service is not running on your virtual machine <!--$vmname-->[vmname]<!--/$vmname-->. This is preventing RDP connectivity to the VM.  The BFE service controls the operation of the Windows Filtering Platform (WFP) which is a network traffic processing platform. If it is not running, network connectivity to the VM will not function correctly.
<!--/issueDescription-->

## **Recommended Steps**
To resolve the issue, please try the steps below using the Azure virtual machine serial console.  If you are unfamiliar with the serial console or would like additional information, please refer to the user [guide](https://docs.microsoft.com/azure/virtual-machines/windows/serial-console).

#### From the Serial Console:

  * Query the state of the service by executing `sc query BFE`
  * If the service is stopped, try starting the service by executing `sc start BFE`
  * If the service is hung with a status starting or stopping, try to stop the service `sc stop BFE` and start it again using `sc start BFE`
  * Once the service is started, set the service startup type to automatic by executing `sc config BFE start= auto`

If the service is not starting due to an error or an issue with dependent processes, a memory dump needs to be collected to continue troubleshooting.
