<properties
pageTitle="No inbound traffic detected"
description="No inbound traffic detected"
infoBubbleText="No inbound traffic detected to the virtual machine"
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani"
displayOrder=""
articleId="InboundTrafficCheck"
diagnosticScenario="Inboundtrafficcheck"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>


# No inbound traffic detected to the virtual machine
<!--issueDescription-->
We have investigated and have detected that there is no inbound traffic to this virtual machine <!--$vmname-->[vmname]<!--/$vmname-->. This usually occurs if the incoming traffic is being blocked from within the guest OS due to an issue with the NIC or some software/policy blocking the incoming traffic.
<!--/issueDescription-->

## **Recommended Steps**

1. Before proceeding further please ensure to take a back up of the OS Disk. This will help if a rollback is required

  * For managed disk VMs, please navigate to the [snapshots blade](https://portal.azure.com/#blade/HubsExtension/Resources/resourceType/Microsoft.Compute%2Fsnapshots) to create a snapshot of the OS disk. For details instructions, see the article [Create a snapshot](https://docs.microsoft.com/azure/virtual-machines/windows/snapshot-copy-managed-disk)<br>
  * For unmanaged VMs save a copy of the OS disk by following the instructions at [Create a copy of a specialized Windows VM running in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized#option-3-copy-an-existing-azure-vm)

2. To regain connectivity to the VM, please try [resetting the NIC](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/reset-network-interface).
3. Reset the Remote Desktop service configuration (https://docs.microsoft.com/azure/virtual-machines/troubleshooting/reset-rdp#reset-the-remote-desktop-service-configuration)
4. Verify the RDP connectivity the VM.

 In case the VM is inaccessible still, a memory dump needs to be collected to continue troubleshooting. If this is the case for you, please email us with your approval to collect a memory dump of this VM and we will investigate further.
