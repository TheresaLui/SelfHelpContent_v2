
<properties
    pageTitle="I can't connect to my Windows VM"
    description="I can't connect to my Windows VM "
    service="microsoft.classiccompute"
    resource="virtualmachines"
    authors="ScottAzure"
    ms.author="scotro
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="windows, WindowsSQL"
    productPesIds=""
    cloudEnvironments="MoonCake"
 	articleId="d21cc1c0-63ee-4096-988e-d531e6d89aed"
	ownershipId="Compute_VirtualMachines"
/>

# I can't connect to my Windows VM

## **Recommended Steps**

1. Verify if your VM is running by viewing your VM's [console screenshot](data-blade:Microsoft_Azure_Classic_Compute.VirtualMachineSerialConsoleLogBlade.id.$resourceId)
2. Ensure that your [Network Security Group](data-blade:microsoft_azure_network.verifyipflowblade.vmId.$resourceId) is allowing traffic
3. [Troubleshoot connectivity issues](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade.id.$resourceId) when trying RDP from Azure
4. Reset Remote Desktop service to fix startup issues with the RDP server by clicking 'Reset Remote' at the top of the VM resource blade
5. [Reset Password](data-blade:Microsoft_Azure_Classic_Compute.PasswordResetBlade.id.$resourceId) to address authentication errors
6. Restart the Virtual Machine to address other startup issues by clicking 'Restart' at the top of the VM resource blade
7. Resize the VM to fix any host issues by clicking 'Size' in the Settings blade of the VM resource

## **Recommended Documents**

* [Troubleshoot specific Remote Desktop connection errors](https://docs.azure.cn/virtual-machines/windows/troubleshoot-rdp-connection#troubleshoot-specific-remote-desktop-connection-errors)<br>
* [Detailed troubleshooting across network components](https://docs.azure.cn/virtual-machines/windows/detailed-troubleshoot-rdp/)<br>
* [Address Remote Desktop License Server error](https://docs.azure.cn/virtual-machines/windows/troubleshoot-specific-rdp-errors#rdplicense)
