<properties
  pagetitle="Azure Stack Marketplace download&#xD;"
  service="microsoft.azurestack"
  resource="registrations"
  ms.author="justinha"
  selfhelptype="Generic"
  supporttopicids="32663924,32737184,32737310,32741946,32745910"
  resourcetags=""
  productpesids="16226,17322,17057,17131,17058"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="ebdc3983-706d-401c-b984-f433c12f1e9f"
  ownershipid="StorageMediaEdge_AzureStack_Hub" />
# Azure Stack Marketplace download

If you are experiencing issues with downloading Azure Stack Hub Marketplace items, apply the latest hotfix, which addresses a known issue where marketplace downloads may fail due to a certificate validation error:

- [2005.20.82](https://support.microsoft.com/help/4592228)
- [2002.61.163](https://support.microsoft.com/help/4592241)
- [1910.84.230](https://support.microsoft.com/help/4592243)
- [1907.33.89](https://support.microsoft.com/help/4562962)
- [1908.59.150](https://support.microsoft.com/help/4592778)

In many other cases, a Marketplace download failure is caused by an underlying problem related to issues such as  insufficient bandwidth or ports blocked by a firewall. Make sure all your settings are correct. If you don't have internet access, see the [prerequisites](https://docs.microsoft.com/azure-stack/operator/azure-stack-download-azure-marketplace-item?view=azs-2002&pivots=state-disconnected) for Azure Stack Hub Marketplace download.

**Common issues**

* If you see a **rainy cloud**, or if you have a Usage Bridge alert, the simplest solution is to [re-register Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-registration) using the same parameters

**Note:** Before you create a support ticket, review [**Release notes**](https://docs.microsoft.com/azure-stack/operator/release-notes) and [**Known issues**](https://docs.microsoft.com/azure-stack/operator/known-issues) for the update you are applying (choose from the Version drop-down menu). This can save you time and effort.

## **Recommended Steps**

1. Check that you have enough bandwidth to download the Marketplace items. In a low bandwidth area, consider using the [disconnected/partially connected method](https://docs.microsoft.com/azure-stack/operator/azure-stack-download-azure-marketplace-item).
2. Check that the [Marketplace syndication endpoints are not blocked by a firewall](https://docs.microsoft.com/azure-stack/operator/azure-stack-integrate-endpoints#ports-and-urls-outbound)
3. Delete the item that failed to download before downloading it again
4. Download one item at a time

There are two scenarios for connecting to the Azure Marketplace:

* Connected scenario
* Disconnected or partially connected scenario

**Note:** In a disconnected environment, you cannot download Marketplace items directly by using the Azure Stack Hub portal. Follow the guide to [download Marketplace items for disconnected or a partially connected scenarios](https://docs.microsoft.com/azure-stack/operator/azure-stack-download-azure-marketplace-item) by using the Marketplace syndication tool and then transferring the items to your Azure Stack Hub environment.

## **Recommended Documents**

* [Download Marketplace items from Azure to Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-download-azure-marketplace-item)
* [Azure Marketplace items for Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-marketplace-azure-items)
