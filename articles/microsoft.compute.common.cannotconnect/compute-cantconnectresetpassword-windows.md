<properties  
    pageTitle="I need to reset my password"
    description="I need to reset my password"
    service=""
    resource=""
    authors="summertgu,scottAzure"
    ms.author="tiag,scotro"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32615529,32639643"
    resourceTags=""
    productPesIds="14749,14745"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="6c04f1f6-0cfe-4a23-bc8a-1f0c2d59aa56"
	ownershipId="Compute_VirtualMachines_Content"
/>

# I need to reset my password

4 out of 5 customers resolved their VM reset password issue using the steps below.<br>

## **Recommended Steps**

If you can't connect to a Windows virtual machine (VM) and suspect the issue would be resolved by resetting the local administrator password, you can reset your local administrator password or reset the Remote Desktop Services (RDS) configuration (not supported on Windows domain controllers). To reset the password, use either the Azure portal or the VM Access extension in Azure PowerShell. After you've signed in to the VM, reset the password for that local administrator.

If you're using Azure PowerShell, make sure that you have the [latest PowerShell module installed](https://docs.microsoft.com/powershell/azure/overview) and configured, and are signed in to your Azure subscription. You can also [perform these steps for VMs created with the classic deployment model](https://docs.microsoft.com/azure/virtual-machines/windows/classic/reset-rdp).

You can reset **Remote Desktop Services** and **credentials** in the following ways:

1. Reading the online documentation:

  * [Resetting the local administrator account password by using the Azure portal](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/reset-rdp#reset-the-local-administrator-account-password)<br>
  * [Resetting the Remote Desktop Services (RDS) configuration by using the Azure portal](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/reset-rdp#reset-the-remote-desktop-services-configuration)<br>


2. Connect to the Azure Portal and **[perform the reset action using the Password Reset Blade](data-blade:Microsoft_Azure_Compute.VirtualMachinePasswordReset.id.$resourceId)**<br>
3. Alternatively, [reset the local administrator account password or RDS configuration by using PowerShell](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/reset-rdp#reset-by-using-the-vmaccess-extension-and-powershell)

If the above fails, you can also use the offline method of [resetting the password by attaching the source OS virtual disk to another VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/reset-local-password-without-agent). **Only use this process as a last resort**. Always try to reset a password using the Azure portal or Azure PowerShell first.

## **Recommended Documents**

* [How to reset the Remote Desktop service or its login password in a Windows VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/reset-rdp)<br>
* [Reset local Windows password for Azure VM using offline method](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/reset-local-password-without-agent)<br>
* [Troubleshooting specific RDP error messages to a Windows VM in Azure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-specific-rdp-errors)<br>
* [Troubleshoot Remote Desktop connections to an Azure Virtual Machine](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-connection)
