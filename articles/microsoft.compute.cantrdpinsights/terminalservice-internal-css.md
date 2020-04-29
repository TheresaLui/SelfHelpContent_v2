<properties
pageTitle="Terminal Service"
description="Terminal Service not running, this service is required to be running for RDP connectivity to the VM"
infoBubbleText="Terminal Service not running this will impact RDP connectivity to the VM"
service="microsoft.compute"
resource="virtualmachines"
authors="timbasham"
ms.author="tibasham"
displayOrder=""
articleId="vmhealthsignal_4c4d26e0-293f-435b-83fe-3ac0169d6cdf"
diagnosticScenario="Terminal Services"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>


# Terminal Service is not running
<!--issueDescription-->
We have investigated and identified that the Terminal Service is not running on this virtual machine <!--$vmname-->[vmname]<!--/$vmname--> impacting RDP connectivity.
<!--/issueDescription-->

## **Recommended Steps**

Before proceeding further please ensure to take a backup of the OS Disk. This will help if a rollback is required.

 * For managed disk VMs: [Create a managed snapshot](https://docs.microsoft.com/azure/virtual-machines/windows/snapshot-copy-managed-disk)
 * For unmanaged disk VMs: [Create a copy of a specialized Windows VM running in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized#option-3-copy-an-existing-azure-vm)

To resolve the issue, please try the steps below using the Azure virtual machine serial console tool.  If you are unfamiliar with the serial console or would like additional information, please refer to the user [guide](https://docs.microsoft.com/azure/virtual-machines/windows/serial-console).

### From the console

  * Query the state of the service by executing `sc query TermService`
  * If the service is stopped, try starting the service by executing `sc start TermService`
  * If the service is hung with a status starting or stopping, try to stop the service `sc stop TermService` and start it again using `sc start TermService`
  * Once the service is started, set the service startup type to automatic by executing `sc config TermService start= auto`

### Using Custom Script Extension

Alternatively, you can run the command `Set-Service -Name TermService -StartupType Manual -status Running` using [Custom Script Extension](https://docs.microsoft.com/azure/virtual-machines/windows/extensions-customscript) to enable the service.

If the service is not starting due to an error or an issue with dependent processes, a memory dump needs to be collected to continue troubleshooting.
