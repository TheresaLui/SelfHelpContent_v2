<properties
    pageTitle="Resolve Windows VM Connection issues"
    description="I can't connect to my Windows VM "
    service="microsoft.classiccompute"
    resource="virtualmachines"
    authors="ScottAzure"
    ms.author="scotro"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds="32615531,32615526,32740112"
    resourceTags="windows,WindowsSQL"
    productPesIds="14749,14745"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="76f3e549-7706-4cc4-870e-b74887a840f7"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Resolve Windows Virtual Machine Connection issues

4 out of 5 customers resolved their VM connectivity issue using the below steps.<br>

## **Recommended Steps**

The following are basic steps to resolve common issues:<br>

1. Verify if your VM is running by viewing your VM's [console screenshot](data-blade:Microsoft_Azure_Classic_Compute.VirtualMachineSerialConsoleLogBlade.id.$resourceId)
2. Click [here](data-blade:microsoft_azure_network.verifyipflowblade.vmId.$resourceId) to ensure that Network Security Group is allowing traffic
3. Click [here](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade.id.$resourceId) to troubleshoot connectivity issues when trying RDP from Azure
4. Reset Remote Desktop service to fix startup issues with the RDP server by clicking 'Reset Remote' at the top of the VM resource blade
5. [Reset Password](data-blade:Microsoft_Azure_Classic_Compute.PasswordResetBlade.id.$resourceId) to address authentication errors
6. Restart the Virtual Machine to address other startup issues by clicking 'Restart' at the top of the VM resource blade
7. Resize the VM to fix any host issues by clicking 'Size' in the Settings blade of the VM resource

## **Recommended Documents**

* [Troubleshoot specific Remote Desktop connection errors](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-connection)<br>
* [Detailed troubleshooting across network components](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/detailed-troubleshoot-rdp/)<br>
* [Address Remote Desktop License Server error](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-no-license-server)
