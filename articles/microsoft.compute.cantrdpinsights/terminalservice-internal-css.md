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
cloudEnvironments="public"
/>


# Terminal Service is not running
<!--issueDescription-->
We have investigated and identified that the Terminal Service is not running on this virtual machine <!--$vmname-->[vmname]<!--/$vmname--> impacting RDP connectivity.
<!--/issueDescription-->

## **Recommended Steps**

1. Before proceeding further please ensure to take a back up of the OS Disk. This will help if a rollback is required.

 * For managed disk VMs, please navigate to the [snapshots blade](https://ms.portal.azure.com/#blade/HubsExtension/Resources/resourceType/Microsoft.Compute%2Fsnapshots) to create a snapshot of the OS disk. For details instructions, see the article [Create a snapshot](https://docs.microsoft.com/azure/virtual-machines/windows/snapshot-copy-managed-disk).
  * For unmanaged VMs save a copy of the OS disk by following the instructions at [Create a copy of a specialized Windows VM running in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized#option-3-copy-an-existing-azure-vm)

2. The VM should have network connectivity though the terminal service is not running
3. To enable the terminal service and start it, connect to the VM from another VM in the same virtual network via [remote powershell](https://docs.microsoft.com/azure/virtual-machines/windows/winrm) or using [PsExec](https://docs.microsoft.com/sysinternals/downloads/pstools)
4. The start mode of the term service needs to be changed to manual (the OS default setting) and the service needs to be started

 * If connected through remote powershell, please run the command `Set-Service -Name TermService -StartupType Manual -status Running` to mitigate the issue and to check if the service has started
 * If using PsExec, please run the below command and specify the admin account user name and enter the password when prompted:

  ```
  PsExec \\<<DIP>> -u "<<userName>>" -s cmd
  REG add "HKLM\SYSTEM\CurrentControlSet\Services\TermService" /v Start /t REG_DWORD /d 3 /f
  ```
5. Alternatively you can run the command `Set-Service -Name TermService -StartupType Manual -status Running` using [Custom Script Extension](https://docs.microsoft.com/azure/virtual-machines/windows/extensions-customscript) to enable the user account
6. Verify the VM now has the RDP connectivity
