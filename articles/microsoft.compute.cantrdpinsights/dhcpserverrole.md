<properties
pageTitle="Unsupported DHCP server role installed"
description="Unsupported DHCP server role installed"
infoBubbleText="Unsupported DHCP server role installed blocking connectivity"
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani"
displayOrder=""
articleId="DHCPServerRole"
diagnosticScenario="DHCPServerRole"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>


# Unsupported DHCP server role installed on the VM
<!--issueDescription-->
We have investigated and identified that DHCP sever role is installed on this VM <!--$vmname-->[vmname]<!--/$vmname--> impacting connectivity. As mentioned in our [public documentation](https://support.microsoft.com/help/2721672/microsoft-server-software-support-for-microsoft-azure-virtual-machines?wa=wsignin1.0) DHCP server role is not supported on Azure virtual machines.
<!--/issueDescription-->

## **Recommended Steps**

1. Before proceeding further please ensure to take a backup of the OS Disk. This will help if a rollback is required.

  * For managed disk VMs, please navigate to the [snapshots blade](https://portal.azure.com/#blade/HubsExtension/Resources/resourceType/Microsoft.Compute%2Fsnapshots) to create a snapshot of the OS disk. For details instructions, see the article [Create a snapshot](https://docs.microsoft.com/azure/virtual-machines/windows/snapshot-copy-managed-disk)<br>
  * For unmanaged VMs save a copy of the OS disk by following the instructions at [Create a copy of a specialized Windows VM running in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized#option-3-copy-an-existing-azure-vm)

2. To resolve this issue, please try the steps below using the Azure virtual machine serial console.  If you’re unfamiliar with the serial console or would like additional information, please refer to our user [guide](https://docs.microsoft.com/azure/virtual-machines/windows/serial-console).

#### From the console: ####

1. From the PowerShell prompt, query the roles of the machine to confirm DHCP role is installed.
```
get-windowsfeature DHCP
```

2. Remove the DHCP role executing the below command and restart the virtual machine.
```
dism /online /disable-feature:DHCP
```

3. Now check if the connectivity to the VM is restored.
