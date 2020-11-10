<properties
pageTitle="IPSec Policy blocking connectivity"
description="IPSec Policy blocking connectivity"
infoBubbleText="IPSec Policy blocking connectivity"
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani"
displayOrder=""
articleId="TrafficBlockedByIPSecPolicy"
diagnosticScenario="TrafficBlockedByIPSecPolicy"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>


# Possible impact to inbound traffic by an IPSec policy
<!--issueDescription-->
We have investigated and identified that an IPSec policy is configured on this virtual machine <!--$vmname-->[vmname]<!--/$vmname--> which can potentially impact the inbound connectivity.
<!--/issueDescription-->

## **Recommended Steps**

1. Before proceeding further please ensure to take a backup of the OS Disk. This will help if a rollback is required

  * For managed disk VMs, please navigate to the [snapshots blade](https://portal.azure.com/#blade/HubsExtension/Resources/resourceType/Microsoft.Compute%2Fsnapshots) to create a snapshot of the OS disk. For details instructions, see the article [Create a snapshot](https://docs.microsoft.com/azure/virtual-machines/windows/snapshot-copy-managed-disk)<br>
  * For unmanaged VMs save a copy of the OS disk by following the instructions at [Create a copy of a specialized Windows VM running in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized#option-3-copy-an-existing-azure-vm)

2. To resolve the issue, please try the steps below using the Azure virtual machine serial console.  If you’re unfamiliar with the serial console or would like additional information, please refer to our user [guide](https://docs.microsoft.com/azure/virtual-machines/windows/serial-console).

#### From the console: ####

1. From the command prompt, query the IPSEC Enforcement configuration to validate if 'IPsec Relying Party client' enforcement is enabled:
 ```
 netsh nap client show configuration
 ```

2. Disable the policy by executing the below command:
 ```
 netsh nap client set enforcement ID = 79619 ADMIN = "DISABLE"
 ```

3. Validate if the connectivity to the VM is restored.
