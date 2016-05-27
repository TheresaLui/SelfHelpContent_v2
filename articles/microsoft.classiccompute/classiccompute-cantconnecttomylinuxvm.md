<properties 
    pageTitle="I can't connect to my Linux VM"
    description="I can't connect to my Linux VM "
    service="microsoft.classiccompute"
    resource="virtualmachines"
    authors="kasparks"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="linux"
    productPesIds=""
	cloudEnvironments="public"
 />

# I can't connect to my Linux VM

## **Recommended steps**
To resolve common isuess, try one or more of the following methods.

1. Review your VM's [console log or screenshot](data-blade:Microsoft_Azure_Classic_Compute.VirtualMachineSerialConsoleLogBlade) to correct boot problems. Review errors in logs such as FSTAB (file systems table), FSCK (file system consistency), or networking.
2. [Reset password](data-blade:Microsoft_Azure_Classic_Compute.PasswordResetBlade) to address authentication errors
3. Restart the virtual machine to address startup issues by clicking 'Restart' at the top of the VM resource blade
4. Resize the VM to fix host issues by clicking 'Size' in the Settings blade of the VM resource
5. Reset the SSH configuration to fix any SSH issues <br>
[Reset SSH using CLI](https://azure.microsoft.com/documentation/articles/virtual-machines-linux-use-vmaccess-reset-password-or-ssh/#sshconfigresetcli)

## **Recommended documents**
[Detailed troubleshooting of SSH errors](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-ssh-connections/#detailed-troubleshooting-of-ssh-errors) <br>
[Automate Linux VM Customization Tasks Using CustomScript Extension](https://azure.microsoft.com/blog/automate-linux-vm-customization-tasks-using-customscript-extension/)