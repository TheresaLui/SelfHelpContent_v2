<properties
pageTitle="Firewall Misconfigured"
description="Firewall Misconfigured"
infoBubbleText="Guest OS firewall profiles were setup to block all inbound connections including the RDP traffic"
service="microsoft.compute"
resource="virtualmachines"
authors="manavis"
ms.author="tibasham"
displayOrder=""
articleId="vmhealthsignal_4d7f5e70-4f1d-48b0-aadd-6bf8e36f3d4a"
diagnosticScenario="Firewall Misconfigured"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>


# Firewall is set to block all inbound connections
<!--issueDescription-->

Guest OS firewall profiles were setup to block all inbound connections including the RDP traffic

<!--/issueDescription-->

## **Recommended Steps**

1. Delete the virtual machine <!--$vmname-->[vmname]<!--/$vmname-->. Make sure that you select the keep the disks option when you do this.
2. Before proceeding further save a copy of the OS disk, this will help in case of a rollback for recovery, see [Create a copy of a specialized Windows VM running in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized#option-3-copy-an-existing-azure-vm)
3. Attach the OS disk of the deleted VM as a data disk to another VM (a troubleshooting VM). For more information, see [How to attach a data disk to a Windows VM in the Azure portal.](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal)
4. Connect to the troubleshooting VM to ensure the newly attached OS disk is online and has a drive letter assigned.
5. On the troubleshooting machine, start registry editor and locate the subtree `HKEY_LOCAL_MACHINE` and click it.
6. Open the File menu and click Load Hive.
7. Locate and click the registry hive `\windows\system32\config\SYSTEM` from the attached OS disk and click open.
8. In the Load Hive dialog box, type a name 'ImpactedVM' in the Key Name box that needs to be edited.
9. Now in the subtree 'ImpactedVM' mounted, delete the following key properties

```
HKLM\ImpactedVM\ControlSet001\services\SharedAccess\Parameters\FirewallPolicy\DomainProfile\DoNotAllowExceptions
HKLM\ImpactedVM\ControlSet001\services\SharedAccess\Parameters\FirewallPolicy\PublicProfile\DoNotAllowExceptions
HKLM\ImpactedVM\ControlSet001\services\SharedAccess\Parameters\FirewallPolicy\StandardProfile\DoNotAllowExceptions
```
**Note**: If this machine has been boot up previously from the Last Known Good configuration, the ControlSet key may be different. To confirm from which ControlKey the machine is booting up check the value of the key `HKLM\BROKENSYSTEM\Select\Current`.
10. Detach the repaired OS disk from the troubleshooting VM. Then [create a new VM from the OS disk](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized)
