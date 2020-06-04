<properties
    pageTitle="Azure Stack Marketplace download"
    description="Azure Stack Marketplace download"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="TobyTu"
    ms.author="mquian"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32663924"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="ebdc3983-706d-401c-b984-f433c12f1e9f"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Marketplace download

**Known issues**

* If you see a "rainy cloud" portal error, the most likely cause is that permissions were removed. To resolve the error, un-register and [register Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-registration). 
* If you see the error message **AADSTS900439: Confidential Client requests are not supported**, the most likely cause is the registration was done with an incorrect endpoint. To resolve the error, un-register and [register Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-registration). 

**NOTE**: Before you create a support ticket, review [**Release notes**](https://docs.microsoft.com/azure-stack/operator/release-notes) and [**Known issues**](https://docs.microsoft.com/azure-stack/operator/known-issues) for the update you are applying (choose from the Version drop-down menu). This may save you time and effort.

## **Recommended Steps**

There are two scenarios for connecting to the Azure Marketplace:

* Connected scenario
* Disconnected or partially connected scenario

**Note :** In a disconnected environment, you cannot download Marketplace items directly by using the Azure Stack Hub portal. Follow the guide to [download Marketplace items for disconnected or a partially connected scenarios](https://docs.microsoft.com/azure-stack/operator/azure-stack-download-azure-Marketplace-item#disconnected-or-a-partially-connected-scenario) by using the Marketplace syndication tool and then transferring the items to your Azure Stack Hub environment.

## **Recommended Documents**

* [Download Marketplace items from Azure to Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-download-azure-Marketplace-item)
* [Azure Marketplace items for Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-marketplace-azure-items)
