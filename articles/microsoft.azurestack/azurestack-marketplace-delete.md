<properties
    pageTitle="Azure Stack Marketplace delete"
    description="Azure Stack Marketplace delete"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="TobyTu"
    ms.author="mquian"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32663923"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax"
    articleId="ebdc1983-706d-401c-b984-f433c12f1e9f"
	ownershipId="ASEP_ContentService_Placeholder"
/>

# Azure Stack Marketplace delete

## **Recommended Steps**

* To verify and update all the Microsoft provided extensions and a set of core images for your Azure Stack, refer [Marketplace Management PowerShell Script](https://azurestack.blog/2018/12/marketplace-management-powershell-script/) and run the scripts
* To remove the Marketplace item, use the following command to first get the list of Marketplace items (you may want to filter those that have the **Publisher** of your VM image in the Marketplace item's name):

   `Get-AzureRMGalleryItem -ApiVersion 2015-04-01`

  From this list, select the Marketplace item for the VM Image that you are trying to delete and then run the following command:

   `Remove-AzureRMGalleryItem -ApiVersion 2015-04-01`
