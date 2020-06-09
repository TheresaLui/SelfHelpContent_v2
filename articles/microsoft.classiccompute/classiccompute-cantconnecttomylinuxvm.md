<properties
    pageTitle="I can't connect to my VM"
    description="I can't connect to my VM "
    service="microsoft.classiccompute"
    resource="virtualmachines"
    authors="ScottAzure"
    ms.author="scotro"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds="32615531,32615526,32639640"
    resourceTags="linux,redhat,Ubuntu"
    productPesIds="16470,15797,15571,16454,16342"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="420298f8-b3fb-49f2-b359-f7cdf357901c"
    category="connectivity"
    searchTags="cannot connect, can't connect, connectivity, vm, rdp"
 	ownershipId="Compute_VirtualMachines"
/>

# I can't connect to my VM

4 out of 5 customers resolved their VM connectivity issue using the below steps.<br>

## **Recommended Steps**

To resolve common issues, try one or more of the following methods:<br>

1. Verify if your VM is running by viewing your VM's [console log or screenshot](data-blade:Microsoft_Azure_Classic_Compute.VirtualMachineSerialConsoleLogBlade.id.$resourceId)

    * Review errors in logs such as FSTAB (file systems table), FSCK (file system consistency), or networking

2. Click [here](data-blade:microsoft_azure_network.verifyipflowblade.vmId.$resourceId) to ensure that Network Security Group is allowing traffic
3. Click [here](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade.id.$resourceId) to troubleshoot connectivity issues when trying SSH from Azure
4. [Reset password](data-blade:Microsoft_Azure_Classic_Compute.PasswordResetBlade.id.$resourceId) to address authentication errors
5. Restart the virtual machine to address startup issues by clicking 'Restart' at the top of the VM resource blade
6. Resize the VM to fix host issues by clicking 'Size' in the Settings blade of the VM resource
7. Reset the SSH configuration to fix any SSH issues [using CLI](https://docs.microsoft.com/azure/virtual-machines/linux/classic/reset-access-classic#sshconfigresetcli)

## **Recommended Documents**

* [Detailed troubleshooting of SSH errors](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/detailed-troubleshoot-ssh-connection)<br>
* [Automate Linux VM Customization Tasks using Custom Script Extension](https://azure.microsoft.com/blog/automate-linux-vm-customization-tasks-using-customscript-extension)
