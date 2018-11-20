<properties  
    pageTitle="I can't connect to my Linux VM"
    description="I can't connect to my Linux VM"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="ScottAzure"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds="32511135,32547978,32547979,32411835,32615531"
    resourceTags="linux,redhat,Ubuntu"
    productPesIds="16342,16065,15797,16454,16470"
    cloudEnvironments="public"
/>

# I can't connect to my Linux VM

4 out of 5 customers resolved their connectivity issue using below steps:<br>

## **Recommended steps**
 To resolve common issues, try one or more of the following steps.

 1. Access [serial console](data-blade:Microsoft_Azure_Compute.SerialConsoleBlade.resourceId.$resourceId) of your VM  and verify if your VM is running . If you prefer you can also see logs by selecting the Boot Diagnostics menu item under the Support + Troubleshooting sub-header for your virtual machine. Review errors in [serial console](data-blade:Microsoft_Azure_Compute.SerialConsoleBlade.resourceId.$resourceId) of your VM  or in logs for errors such as FSTAB (file systems table), FSCK (file system consistency), or networking
 2. Click [here](data-blade:microsoft_azure_network.verifyipflowblade.vmId.$resourceId) to ensure that Network Security Group is allowing traffic
 3. Click [here](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade.id.$resourceId) to troubleshoot connectivity issues when trying SSH from Azure
 4. Review effective security group rules to ensure inbound “Allow” NSG rule exists and is prioritized for SSH port(default 22)
 5. Reset Password to address authentication errors <br>
 [Reset Password using CLI or PowerShell](http://aka.ms/resetarmpass)
 6. Restart the Virtual Machine to address startup issues by clicking 'Restart' at the top of the VM resource blade
 7. Reset the SSH connection and configuration to fix SSH issues <br>
 [Reset SSH connection using CLI](http://aka.ms/resetarmssh)
 8. SSH to your VM from Internet may not work with forced tunneling enabled. Review [effective routes](data-blade:Microsoft_Azure_Network.EffectiveRoutesBlade.id.$resourceId). With forced tunneling, all outbound traffic destined to Internet will be redirected to on-premises
 9. Address any Azure host issues by [redeploying](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeployViewModel.id.$resourceId), which will migrate the VM to a new Azure host

## **Recommended documents**

* [Detailed troubleshooting of SSH errors](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-ssh-connections/#detailed-troubleshooting-of-ssh-errors) <br>
* [Automate Linux VM Customization Tasks Using CustomScript Extension](https://azure.microsoft.com/blog/automate-linux-vm-customization-tasks-using-customscript-extension/)
