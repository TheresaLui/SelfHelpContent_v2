<properties
    pageTitle="Azure Stack virtual machine settings"
    description="Resolve issues with Azure Stack virtual machine settings"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629226"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-vm-settings"
/>

# Azure Stack modify virtual machine settings

One of the great benefits of Azure VMs is the ability to change the size of your VM based on the needs for CPU, Network, or disk performance. You can modify a number of settings for your VM.

## **Recommended steps**

- After you create a virtual machine (VM), you can scale the VM up or down by changing the VM size. In some cases, you must de-allocate the VM first. For more information, see [Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm)
- If you have an existing VM, but you want to swap the disk for a backup disk or another OS disk, you can [Change the OS disk used by an Azure VM using PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/os-disk-swap
)
- The following steps describe how to change the availability set of a VM using Azure PowerShell. A VM can only be added to an availability set when it is created. For more information, see [Change the availability set for a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/change-availability-set)
- Redeploy a VM
    For more information, see [Linux](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-linux)
    For more information, see [Windows](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-windows)
- [Restarting or resizing a VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/restart-resize-error-troubleshooting)
- [Device names are changed](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-device-names-problems)

## **Recommended documents**

- [Troubleshooting Azure virtual machines](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/)
- [Considerations for using virtual machines in Azure Stack ](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-vm-considerations)