
<properties 
    pageTitle="I can't connect to my Windows VM"
    description="I can't connect to my Windows VM "
    service="microsoft.classiccompute"
    resource="virtualmachines"
    authors="kasparks"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="windows"
    productPesIds=""
	cloudEnvironments="public"
 />
    
# I can't connect to my Windows VM

## **Recommended steps**

The following are basic steps to resolve common issues.

1. Review your VM's [console screenshot](data-blade:Microsoft_Azure_Classic_Compute.VirtualMachineSerialConsoleLogBlade) to correct boot problems
2. Reset Remote Desktop service to fix startup issues with the RDP server by clicking 'Reset Remote' at the top of the VM resource blade
3. [Reset Password](data-blade:Microsoft_Azure_Classic_Compute.PasswordResetBlade) to address authentication errors
4. Restart the Virtual Machine to address other startup issues by clicking 'Restart' at the top of the VM resource blade
5. Resize the VM to fix any host issues by clicking 'Size' in the Settings blade of the VM resource

## **Recommended documents**
[Troubleshoot specific Remote Desktop connection errors](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-remote-desktop-connections/#troubleshoot-specific-remote-desktop-connection-errors) <br>
[Detailed troubleshooting across network components](https://azure.microsoft.com/documentation/articles/virtual-machines-rdp-detailed-troubleshoot/) <br>
[Address Remote Desktop License Server error](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-remote-desktop-connections/#rdplicense) 