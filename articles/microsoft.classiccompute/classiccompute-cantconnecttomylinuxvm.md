<properties
    pageTitle="I can't connect to my Linux VM"
    description="I can't connect to my Linux VM "
    service="microsoft.classiccompute"
    resource="virtualmachines"
    authors="kasparks"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds="32411835,32602159"
    resourceTags="linux"
    productPesIds="16470,15797,15571"
    cloudEnvironments="public"
 />

# I can't connect to my Linux VM

## **Recommended steps**
To resolve common issues, try one or more of the following methods.

1. Verify if your VM is running by viewing your VM's [console log or screenshot](data-blade:Microsoft_Azure_Classic_Compute.VirtualMachineSerialConsoleLogBlade). Review errors in logs such as FSTAB (file systems table), FSCK (file system consistency), or networking.
2. Click [here](data-blade:microsoft_azure_network.verifyipflowblade) to ensure that Network Security Group is allowing traffic
3. Click [here](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade) to troubleshoot connectivity issues when trying SSH from Azure
4. [Reset password](data-blade:Microsoft_Azure_Classic_Compute.PasswordResetBlade) to address authentication errors
5. Restart the virtual machine to address startup issues by clicking 'Restart' at the top of the VM resource blade
6. Resize the VM to fix host issues by clicking 'Size' in the Settings blade of the VM resource
7. Reset the SSH configuration to fix any SSH issues <br>
[Reset SSH using CLI](https://docs.microsoft.com/azure/virtual-machines/linux/classic/reset-access-classic#sshconfigresetcli)

## **Recommended documents**
[Detailed troubleshooting of SSH errors](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-ssh-connections/#detailed-troubleshooting-of-ssh-errors) <br>
[Automate Linux VM Customization Tasks Using CustomScript Extension](https://azure.microsoft.com/blog/automate-linux-vm-customization-tasks-using-customscript-extension/)
