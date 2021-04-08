<properties
    pageTitle="Azure Stack windows-based virtual machines"
    description="Issues with Windows Based Virtual machines"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32663892"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-vm-windows"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Windows-based virtual machines

You can deploy Windows Server VM images on Azure Stack by adding a Windows-based image in the Azure Stack Hub Marketplace. The easiest way to add a Windows image to Azure Stack is through Marketplace Management. These images have been prepared and tested for compatibility with Azure Stack.

Most users could resolve issues by using the following steps.<br>

## **Recommended Steps**

1. Choose a [Windows image](https://docs.microsoft.com/azure/azure-stack/azure-stack-marketplace-azure-items#microsoft-virtual-machine-images-and-solution-templates) and [download it to the Azure Stack Hub Marketplace](https://docs.microsoft.com/azure/azure-stack/azure-stack-download-azure-marketplace-item)
1. For ARM deployments, you can create a [custom image and upload it](https://docs.microsoft.com/azure-stack/operator/azure-stack-add-vm-image) to the marketplace
1. If you upload a custom image, you need to create a [VM marketplace item](https://docs.microsoft.com/azure-stack/operator/azure-stack-create-and-publish-marketplace-item) to make it visible to all tenant users
1. If VM activation is failing, see [Troubleshoot virtual machines](https://docs.microsoft.com/azure-stack/operator/azure-stack-troubleshooting#troubleshoot-virtual-machines-vms)

## Moving or migrating VMs

- See [this overview of moving](https://docs.microsoft.com/azure-stack/user/vm-move-overview) your Azure or local Hyper-V VM to Azure Stack Hub
- For instructions on generalizing and moving your Windows VM, see [Move a generalized VM from on-premises to Azure Stack Hub](https://docs.microsoft.com/azure-stack/user/vm-move-generalized)

## Troubleshooting VMs

- For troubleshooting a VHD that you are moving, see [Verify your VHD](https://docs.microsoft.com/azure-stack/user/vm-move-from-azure?view=azs-2005&tabs=win-spec%2Ccreate-vm-spec#verify-your-vhd)
- For general VM troubleshooting guidance, see [Troubleshoot Windows virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/)

## Change drive letter for temp drive

If your application needs to use the a drive to store data, follow these instructions to use a different drive letter for the temporary disk: [Use the D: drive as a data drive on a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/change-drive-letter).

## Activation issues for Microsoft Windows 2008 Server

You can access an update that enables the VAMT tool to deploy and activate keys for Windows Server 2008, Windows Server 2008 R2, Windows 7 SP1 Extended Security Update programs. To download the tool, see [VAMT- ESU Configuration](https://www.microsoft.com/download/details.aspx?id=100304).


## **Recommended Documents**

* [Windows Virtual Machines Documentation](https://docs.microsoft.com/azure/virtual-machines/windows/)
* [Make a virtual machine image available in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-vm-image)
* [Considerations for using virtual machines in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-vm-considerations)
* [Known Issues: VMs on Azure Stack Hub](https://docs.microsoft.com/azure-stack/user/troubleshoot-vm-known-issues)
