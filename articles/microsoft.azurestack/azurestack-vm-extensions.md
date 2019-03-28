<properties
    pageTitle="Azure Stack virtual machine (VM) extensions"
    description=""
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629275"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-vm-extensions"
/>

# Azure Stack virtual machine (VM) extensions

Azure virtual machine (VM) extensions are small applications that provide post-deployment configuration and automation tasks on Azure VMs, you can use existing images and then customize them as part of your deployments, getting you out of the business of custom image building.

## **Recommended steps**

1. You can view available extensions in the VM blade in the Portal, under extensions, this represents just a small amount, for the full list, you can use the CLI tools, see [Discovering VM Extensions for Linux](https://docs.microsoft.com/en-us/azure/virtual-machines/extensions/features-linux) and [Discovering VM Extensions for Windows](https://docs.microsoft.com/en-us/azure/virtual-machines/extensions/features-windows).<br>
2. You can view the extensions available in Azure Stack via the administrative portal. See [Azure Marketplace items available for Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-marketplace-azure-items).<br>
2. Azure VM extensions can be managed using either the Azure CLI, Azure PowerShell, Azure Resource Manager templates, and the Azure portal. To try an extension, you can go to the Azure portal, select the Custom Script Extension, then pass in a command / script and run the extensions.<br>
3. You do not need to connect to a VM directly to install or delete the extension. As the Azure extension application lifecycle is managed outside of the VM and integrated into the Azure platform, you also get integrated status of the extension.<br>
4. Extensions install applications, like any applications there are some requirements, for extensions there is a list of supported Windows and Linux OSes, and you need to have the Azure VM agents installed. Some individual VM extension applications may have their own environmental prerequisites, such as access to an endpoint.<br>

## **Recommended documents**

[Download marketplace items from Azure to Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-download-azure-marketplace-item)<br>
[Azure Marketplace items available for Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-marketplace-azure-items)<br>
[Azure virtual machine extensions and features](https://docs.microsoft.com/en-us/azure/virtual-machines/extensions/overview)