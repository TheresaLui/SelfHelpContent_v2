<properties
    pageTitle="Azure Stack virtual machine settings"
    description="Resolve issues with Azure Stack virtual machine settings"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32663898,32663899"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-vm-settings"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Modifying Azure Stack Virtual Machine Settings

Azure Stack has the ability to change the size of your VM based on the needs for CPU, Network, or disk performance. You can modify size, as well as a number of other settings for your VM.

4 out of 5 customers resolved their issue using the guides listed below.<br>

## **Recommended Steps**

- Review supported [VM sizes for Azure Stack](https://docs.microsoft.com/azure-stack/user/azure-stack-vm-sizes)<br>
- After you create a virtual machine (VM), you can scale the VM up or down by using steps to [resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm)<br>
- If you have an existing VM, but you want to swap the disk for a backup disk or another OS disk, you can [change the OS disk used by an Azure VM](https://docs.microsoft.com/azure/virtual-machines/windows/os-disk-swap)<br>
- A VM can only be added to one availability set when it is created, but you can [change the availability set for a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/change-availability-set) on Azure Stack using Azure PowerShell<br>
- When you redeploy a VM, it moves the VM to a new node within the Azure Stack infrastructure and all your configuration options and associated resources are retained, see steps to redeploy a [Linux](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-linux) or [Windows](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-windows) VM <br>

## **Recommended Documents**

- [VM sizes supported in Azure Stack](https://docs.microsoft.com/azure-stack/user/azure-stack-vm-sizes)<br>
- [Restarting or resizing a VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/restart-resize-error-troubleshooting)<br>
- [Troubleshooting Azure virtual machines](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/)<br>
- [Troubleshoot Linux VM Device Name Changes](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-device-names-problems)<br>
- [Considerations for using virtual machines in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-vm-considerations)<br>
- [Virtual machine memory allocation and placement on Azure Stack](https://azure.microsoft.com/blog/virtual-machine-memory-allocation-and-placement-on-azure-stack/)<br>
- [Azure VM disk FAQ](https://docs.microsoft.com/azure/virtual-machines/windows/faq-for-disks)

