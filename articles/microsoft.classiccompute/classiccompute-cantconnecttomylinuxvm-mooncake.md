<properties
    pageTitle="I can't connect to my Linux VM"
    description="I can't connect to my Linux VM "
    service="microsoft.classiccompute"
    resource="virtualmachines"
    authors="ScottAzure"
    ms.author="scotro
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="linux"
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="bb60fd9c-6e0c-409e-a3cd-d7a04cfb2339"
	ownershipId="Compute_VirtualMachines"
/>

# I can't connect to my Linux VM

## **Recommended Steps**

To resolve common issues, try one or more of the following methods:<br>

1. Verify if your VM is running by viewing your VM's [console log or screenshot](data-blade:Microsoft_Azure_Classic_Compute.VirtualMachineSerialConsoleLogBlade.id.$resourceId).

    * Review errors in logs such as FSTAB (file systems table), FSCK (file system consistency), or networking.<br>

2. Click [here](data-blade:microsoft_azure_network.verifyipflowblade.vmId.$resourceId) to ensure that Network Security Group is allowing traffic.<br>
3. Click [here](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade.id.$resourceId) to troubleshoot connectivity issues when trying SSH from Azure.<br>
4. [Reset password](data-blade:Microsoft_Azure_Classic_Compute.PasswordResetBlade.id.$resourceId) to address authentication errors.<br>
5. Restart the virtual machine to address startup issues by clicking 'Restart' at the top of the VM resource blade.<br>
6. Resize the VM to fix host issues by clicking 'Size' in the Settings blade of the VM resource.<br>
7. Reset the SSH configuration to fix any SSH issues [using CLI](https://docs.azure.cn/virtual-machines/linux/classic/reset-access-classic#sshconfigresetcli).

## **Recommended Documents**

* [Detailed troubleshooting of SSH errors](https://docs.azure.cn/virtual-machines/linux/troubleshoot-ssh-connection#detailed-troubleshooting-of-ssh-errors)<br>
* [Automate Linux VM Customization Tasks Using CustomScript Extension](https://www.azure.cn/blog/2014/09/11/automate-linux-vm-customization-tasks-using-customscript-extension/)
