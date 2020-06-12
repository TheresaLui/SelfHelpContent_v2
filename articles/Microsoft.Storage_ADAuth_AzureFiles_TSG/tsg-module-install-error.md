<properties
    pageTitle="Customer faces issues while setting up Hybrid PowerShell module"
    description="Customer faces issues while setting up Hybrid PowerShell module"
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="TSG_Content"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="6324651b-9bb3-4312-9b5e-4519d3a7ce8e"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Customer faces issues while setting up Hybrid PowerShell module

It is common for customers to run into errors when attempting to domain join an Azure storage account.  The process to domain join a storage account using PowerShell can be found [here](https://docs.microsoft.com/azure/storage/files/storage-files-identity-ad-ds-enable).  In order to run the script provided in our public documentation, the machine being used to execute the PowerShell commands must meet the following minimum prerequisites:

1. .Net Framework: 4.7.2 or above
2. PowerShell: 5.1 or Above
3. [Az Module Installed](https://docs.microsoft.com/powershell/azure/new-azureps-module-az?view=azps-3.6.1)
4. [PowerShellGet Module Installed](https://docs.microsoft.com/powershell/scripting/gallery/installing-psget?view=powershell-7)
5. [Az.Storage Module: 1.11.1-preview](https://www.powershellgallery.com/packages/Az.Storage/2.0.0)

*Note:  In most cases Az, PowerShellGet and Az.Storage will be installed as part of importing the AzFileHybrid module.  
## How to check PowerShell Version

Run "$PSVersionTable.PSVersion" from a PowerShell Console. 

## How to check the .Net version

Check .Net version by looking at the "Version" registry key under this path - 
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full

## PowerShell 5.1 Requirements   

Windows PowerShell runs on the [these versions of Windows](https://docs.microsoft.com/powershell/scripting/install/windows-powershell-system-requirements?view=powershell-7#operating-system-requirements).

## Az Module Requirements
Az Module have the following prerequisites. 

1. Windows PowerShell 5.1 or higher
2. .NET Framework 4.7.2 or higher
3. Latest version of PowerShellGet - Update-Module PowerShellGet -Force

## Update to .Net Framework 4.7.2

https://support.microsoft.com/help/4054530/microsoft-net-framework-4-7-2-offline-installer-for-windows

Please make sure customer's environment has the above prerequisites in place and see if they are facing any of the following errors.
