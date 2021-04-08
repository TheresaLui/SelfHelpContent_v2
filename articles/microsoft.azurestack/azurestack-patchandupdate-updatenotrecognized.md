<properties
  pagetitle="Azure Stack Patch and Update Not Recognized&#xD;"
  service="microsoft.azurestack"
  resource="azurestack"
  ms.author="alexsmit,patricka"
  selfhelptype="Generic"
  supporttopicids="32629272"
  resourcetags=""
  productpesids="16226"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azurestack-patchandupdate-updatenotrecognized"
  ownershipid="StorageMediaEdge_AzureStack_Hub" />
# Azure Stack Patch and Update Not Recognized

Customers with Azure Stack environments connected to the internet will automatically see **Update Available** in the Admin Portal. For customers that aren't connected to the internet, get update release notifications via RSS feed at [Support Content Updates](https://support.microsoft.com/help/4089498/support-content-updates). Select Product as **Azure Stack**, and choose ATOM or RSS.

## **Recommended Steps**

1. Review the release notes of the specific update package for any known issues. This is listed under [Update Package Release Cadence](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence).
2. If the update is marked as **Not Recognized**, try manually importing the update package with the [Import and install updates instructions](https://docs.microsoft.com/azure-stack/operator/azure-stack-update-prepare-package?view=azs-2005). If you have already attempted importing the update package manually, delete the blob container from your previous attempt before reimporting the package.
3. If the update is still **Not Recognized** after a retry, continue to open a support case

## **Recommended Documents**

* [Azure Stack servicing policy - Recent Update](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence)
* [Manage updates in Azure Stack overview](https://docs.microsoft.com/azure/azure-stack/azure-stack-updates)
* [Monitor updates in Azure Stack using the privileged endpoint](https://docs.microsoft.com/azure/azure-stack/azure-stack-monitor-update)
* [Use REST to get update status](https://docs.microsoft.com/rest/api/azurestack/updates/get#updatestate)
