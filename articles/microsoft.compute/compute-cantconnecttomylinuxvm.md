<properties  
    pageTitle="Resolve connection issue with your Linux VM"
    description="Resolve connection issue with your Linux VM"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="ScottAzure,timbasham"
    ms.author="scotro,tibasham"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds="32547978,32547979,32615531,32615526,32639640,32615530,32675597,32675600,32675601,32675599"
    resourceTags="linux,redhat,Ubuntu"
    productPesIds="15571,16342,16065,15797,16454,16470"
    cloudEnvironments="public, Mooncake, Fairfax, usnat, ussec"
    articleId="51356b1f-09f5-4a5b-85f4-dc96cea89c14"
	ownershipId="Compute_VirtualMachines"
/>

# Resolve connection issue with your Linux VM

4 out of 5 customers resolved their VM connectivity issue using the steps listed below.

## **Recommended Steps**

To resolve common issues, try one or more of the following:

1. Access [Serial console](data-blade:Microsoft_Azure_Compute.VmSerialConsoleValidationBlade.resourceId.$resourceId) of your VM  and verify if your VM is running. If you prefer, you can also see logs by selecting the Boot Diagnostics menu item under the Support + Troubleshooting sub-header for your virtual machine.
1. Review errors in [serial console](data-blade:Microsoft_Azure_Compute.VmSerialConsoleValidationBlade.resourceId.$resourceId) of your VM or in logs for errors such as [FSTAB](https://support.microsoft.com/help/3206699/azure-linux-vm-cannot-start-because-of-fstab-errors) (file systems table), [FSCK](https://support.microsoft.com/help/3213321/linux-recovery-cannot-ssh-to-linux-vm-due-to-file-system-errors-fsck) (file system consistency), or networking
1. Try using [Azure Bastion](data-blade:Microsoft_Azure_HybridNetworking.BastionHostBlade.resourceId.$resourceId) to connect to your VM.  [Azure Bastion](https://docs.microsoft.com/azure/bastion/bastion-overview) provides secure and seamless RDP connectivity to your virtual machine directly in the Azure portal over TLS. When you connect via Azure Bastion, your virtual machine does not need a public IP address, or inbound NSG rule allowing RDP traffic.
1. [Validate your Network Security Group is allowing traffic](data-blade:microsoft_azure_network.verifyipflowblade.vmId.$resourceId)
1. [Troubleshoot connectivity issues when trying SSH from Azure](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade.id.$resourceId)
1. Review effective security group rules to ensure inbound "Allow" NSG rule exists and is prioritized for SSH port (default 22)
1. [Reset Password using CLI or PowerShell](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-ssh-connection)
1. Restart the Virtual Machine to address startup issues by clicking 'Restart' at the top of the VM resource blade
1. [Reset SSH connection and configuration using CLI](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-ssh-connection) to fix SSH issues
1. SSH to your VM from Internet may not work with forced tunneling enabled. Review [effective routes](data-blade:Microsoft_Azure_Network.EffectiveRoutesBlade.id.$resourceId). With forced tunneling, all outbound traffic destined to Internet will be redirected to on-premises
1. Address any Azure host issues by [redeploying](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeployViewModel.id.$resourceId), which will migrate the VM to a new Azure host

## **Recommended Documents**

* [Detailed troubleshooting of SSH errors](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/detailed-troubleshoot-ssh-connection) <br>
* [Automate Linux VM Customization Tasks using Custom Script Extension](https://azure.microsoft.com/blog/automate-linux-vm-customization-tasks-using-customscript-extension/)
* [Troubleshooting a Linux VM that is using LVM and is not booting](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/chroot-logical-volume-manager)
