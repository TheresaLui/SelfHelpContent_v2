<properties  
    pageTitle="I can't connect to my Linux VM"
    description="I can't connect to my Linux VM"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="ScottAzure"
    ms.author="scotro"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds="32511135,32547978,32547979,32615531,32615526"
    resourceTags="linux,redhat,Ubuntu"
    productPesIds="15571,16342,16065,15797,16454,16470"
    cloudEnvironments="public"
	articleId="51356b1f-09f5-4a5b-85f4-dc96cea89c14"
/>

# I can't connect to my Linux VM

4 out of 5 customers resolved their VM connectivity issue using the steps listed below.

## **Recommended Steps**

To resolve common issues, try one or more of the following:

1. Access [Serial console](data-blade:Microsoft_Azure_Compute.SerialConsoleBlade.resourceId.$resourceId) of your VM  and verify if your VM is running. If you prefer, you can also see logs by selecting the Boot Diagnostics menu item under the Support + Troubleshooting sub-header for your virtual machine.
2. Review errors in [serial console](data-blade:Microsoft_Azure_Compute.SerialConsoleBlade.resourceId.$resourceId) of your VM or in logs for errors such as FSTAB (file systems table), FSCK (file system consistency), or networking
3. [Validate your Network Security Group is allowing traffic](data-blade:microsoft_azure_network.verifyipflowblade.vmId.$resourceId)
4. [Troubleshoot connectivity issues when trying SSH from Azure](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade.id.$resourceId)
5. Review effective security group rules to ensure inbound “Allow” NSG rule exists and is prioritized for SSH port (default 22)
6. [Reset Password using CLI or PowerShell](http://aka.ms/resetarmpass)
7. Restart the Virtual Machine to address startup issues by clicking 'Restart' at the top of the VM resource blade
8. [Reset SSH connection and configuration using CLI](http://aka.ms/resetarmssh) to fix SSH issues
9. SSH to your VM from Internet may not work with forced tunneling enabled. Review [effective routes](data-blade:Microsoft_Azure_Network.EffectiveRoutesBlade.id.$resourceId). With forced tunneling, all outbound traffic destined to Internet will be redirected to on-premises
10. Address any Azure host issues by [redeploying](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeployViewModel.id.$resourceId), which will migrate the VM to a new Azure host

## **Recommended Documents**

* [Detailed troubleshooting of SSH errors](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-ssh-connections/#detailed-troubleshooting-of-ssh-errors) <br>
* [Automate Linux VM Customization Tasks using Custom Script Extension](https://azure.microsoft.com/blog/automate-linux-vm-customization-tasks-using-customscript-extension/)
