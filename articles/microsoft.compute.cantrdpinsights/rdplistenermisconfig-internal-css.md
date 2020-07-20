<properties
pageTitle="RDPListener misconfigured"
description="RDP-TCP listener misconfigured"
infoBubbleText="RDP-TCP listener misconfigured"
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani"
displayOrder=""
articleId="vmhealthsignal_451e7e7e-0aae-4145-ae1b-e761548a36d7"
diagnosticScenario="RDP listener"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>


# RDP-TCP listener is misconfigured
<!--issueDescription-->
We have investigated and identified that the RDP-TCP listener is misconfigured impacting RDP connectivity to this virtual machine <!--$vmname-->[vmname]<!--/$vmname-->. Reconfigure the listener via serial console or other remote management options described below to regain RDP connectivity
<!--/issueDescription-->

## **Recommended Steps**

1. Before proceeding further please ensure to take a back up of the OS Disk. This will help if a rollback is required

  * For managed disk VMs, please navigate to the [snapshots blade](https://ms.portal.azure.com/#blade/HubsExtension/Resources/resourceType/Microsoft.Compute%2Fsnapshots) to create a snapshot of the OS disk. For details instructions, see the article [Create a snapshot](https://docs.microsoft.com/azure/virtual-machines/windows/snapshot-copy-managed-disk)
  * For unmanaged VMs save a copy of the OS disk by following the instructions at [Create a copy of a specialized Windows VM running in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized#option-3-copy-an-existing-azure-vm)

2. To regain connectivity to the VM, RDP-TCP Listener needs to be reconfigured using one of the below ways.

 * Login using the [Serial Console](http://aka.ms/serialconsolehelp)
 * Using [Custom Script Extension](https://docs.microsoft.com/azure/virtual-machines/windows/extensions-customscript)
 * Connect to the VM from another VM in the same virtual network via
    * [remote powershell](https://docs.microsoft.com/azure/virtual-machines/windows/winrm)
    * Using [PsExec](https://docs.microsoft.com/sysinternals/downloads/pstools)

3. Below the registry key settings that need to be changed:

 ```
 Set-ItemProperty -Path 'HKLM:\SYSTEM\CurrentControlSet\Control\Terminal Server\WinStations\RDP-Tcp' -name "SecurityLayer" -value 0
 Set-ItemProperty -Path 'HKLM:\SYSTEM\CurrentControlSet\Control\Terminal Server\WinStations\RDP-Tcp' -name "UserAuthentication" -value 0
 Set-ItemProperty -Path 'HKLM:\SYSTEM\CurrentControlSet\Control\Terminal Server\WinStations\RDP-Tcp' -name "fAllowSecProtocolNegotiation" -value 0

 ```
4. Verify the VM now has the RDP connectivity.
