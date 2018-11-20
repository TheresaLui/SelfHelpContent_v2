<properties
    pageTitle="I can't connect to my Windows VM"
    description="I can't connect to my Windows VM "
    service="microsoft.classiccompute"
    resource="virtualmachines"
    authors="ScottAzure"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds="32411835,32615531,32615526"
    resourceTags="windows, WindowsSQL"
    productPesIds="14749"
    cloudEnvironments="public"
 />

# I can't connect to my Windows VM

4 out of 5 customers resolved their connectivity issue using below steps:<br>

## **Recommended steps**

The following are basic steps to resolve common issues:<br>

1. Verify if your VM is running by viewing your VM's [console screenshot](data-blade:Microsoft_Azure_Classic_Compute.VirtualMachineSerialConsoleLogBlade.id.$resourceId).<br>
2. Click [here](data-blade:microsoft_azure_network.verifyipflowblade.vmId.$resourceId) to ensure that Network Security Group is allowing traffic.<br>
3. Click [here](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade.id.$resourceId) to troubleshoot connectivity issues when trying RDP from Azure.<br>
4. Reset Remote Desktop service to fix startup issues with the RDP server by clicking 'Reset Remote' at the top of the VM resource blade.<br>
5. [Reset Password](data-blade:Microsoft_Azure_Classic_Compute.PasswordResetBlade.id.$resourceId) to address authentication errors.<br>
6. Restart the Virtual Machine to address other startup issues by clicking 'Restart' at the top of the VM resource blade.<br>
7. Resize the VM to fix any host issues by clicking 'Size' in the Settings blade of the VM resource.

## **Recommended documents**

* [Troubleshoot specific Remote Desktop connection errors](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-remote-desktop-connections/#troubleshoot-specific-remote-desktop-connection-errors)<br>
* [Detailed troubleshooting across network components](https://azure.microsoft.com/documentation/articles/virtual-machines-rdp-detailed-troubleshoot/)<br>
* [Address Remote Desktop License Server error](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-remote-desktop-connections/#rdplicense)
