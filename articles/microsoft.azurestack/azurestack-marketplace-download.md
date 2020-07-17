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

In many cases, a Marketplace download failure is caused by an underlying problem related to things like insufficient bandwidth or ports blocked by firewall. Make sure all your settings are correct. If you don't have internet access, see the [prerequisites](https://docs.microsoft.com/azure-stack/operator/azure-stack-download-azure-marketplace-item?view=azs-2002&pivots=state-disconnected) for Azure Stack Hub Marketplace download.

**Common issues**

* If you see a **rainy cloud**, or if you have a Usage Bridge alert, the simplest solution is to [re-register Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-registration) using the same parameters.

**NOTE**: Before you create a support ticket, review [**Release notes**](https://docs.microsoft.com/azure-stack/operator/release-notes) and [**Known issues**](https://docs.microsoft.com/azure-stack/operator/known-issues) for the update you are applying (choose from the Version drop-down menu). This may save you time and effort.

## **Recommended Steps**

There are two scenarios for connecting to the Azure Marketplace:

* Connected scenario
* Disconnected or partially connected scenario

**Note:** In a disconnected environment, you cannot download Marketplace items directly by using the Azure Stack Hub portal. Follow the guide to [download Marketplace items for disconnected or a partially connected scenarios](https://docs.microsoft.com/azure-stack/operator/azure-stack-download-azure-marketplace-item) by using the Marketplace syndication tool and then transferring the items to your Azure Stack Hub environment.

1. Some of the images offered on the marketplace are quite large (> 100GB). Make sure that you have high bandwidth connectivity to avoid timeout failures.

   In a low bandwidth area, consider using the [disconnected/partially connected method](https://docs.microsoft.com/azure-stack/operator/azure-stack-download-azure-marketplace-item).

2. Marketplace images can also fail to download if the endpoints for marketplace syndication are being blocked by a firewall. Please see the [publishing endpoints documentation](https://docs.microsoft.com/azure-stack/operator/azure-stack-integrate-endpoints#ports-and-urls-outbound) to ensure the appropriate ports and URLs are unblocked for outbound connections.

3. Azure Stack Hub does not support SSL interception. Please ensure that no proxy devices intercept any outbound SSL traffic.

4. If a marketplace image is in a failed state, delete the image before retrying the download.

## **Recommended Documents**

* [Download Marketplace items from Azure to Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-download-azure-marketplace-item)
* [Azure Marketplace items for Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-marketplace-azure-items)
