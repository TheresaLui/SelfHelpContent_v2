<properties
pageTitle="Terminal Service"
description="Terminal Service not running"
infoBubbleText="Terminal Service not running"
service="microsoft.compute"
resource="virtualmachines"
authors="manavis"
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
Terminal Service is not running and hence RDP connectivity is impacted
<!--/issueDescription-->

## **Customer Ready Mitigation Steps**

1. Before proceeding further please ensure to take a back up of the OS Disk. This will help if a rollback is required <br>
  * For managed disk VMs, please navigate to the [snapshots blade](https://ms.portal.azure.com/#blade/HubsExtension/Resources/resourceType/Microsoft.Compute%2Fsnapshots) to create a snapshot of the OS disk. For details instructions, see the article [Create a snapshot](https://docs.microsoft.com/azure/virtual-machines/windows/snapshot-copy-managed-disk)<br>
  * For unmanaged VMs save a copy of the OS disk by following the instructions at [Create a copy of a specialized Windows VM running in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized#option-3-copy-an-existing-azure-vm)
2. The VM should have network connectivity though the terminal service is not running.
3. So to enable the terminal service and start it, connect to the VM from another VM in the same virtual network via [remote powershell](https://docs.microsoft.com/azure/virtual-machines/windows/winrm) or using [PsExec](https://docs.microsoft.com/sysinternals/downloads/pstools)
4. The start mode of the term service needs to be changed to auto and the service need to be started.
  * If connected through remote powershell, please run the below command to mitigate the issue and to check if the service has started.
  ```
set-Service -Name termservice -StartupType automatic -status Running
  ```
  * If using PsExec, please run the below command and specify the admin account user name and enter the password when prompted.
  ```
  PsExec \\<<DIP>> -u "<<userName>>" -s cmd
REG add "HKLM\SYSTEM\CurrentControlSet\services\netlogon" /v Start /t REG_DWORD /d 2 /f
  ```
5. Alternatively you can run the command below using [Custom Script Extension](https://docs.microsoft.com/azure/virtual-machines/windows/extensions-customscript) to enable the user account:
```
set-Service -Name termservice -StartupType automatic -status Running
```
6. Verify the VM now has the RDP connectivity.

## **Internal**

For more details, refer to the [internal article](https://www.csssupportwiki.com/index.php/curated:Azure/Virtual_Machine/Can%E2%80%99t_RDP-SSH/TSG/VM_Responding_Bucket/TermService_service_is_not_starting).
