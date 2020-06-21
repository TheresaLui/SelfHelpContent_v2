<properties
    pageTitle="Azure Stack Patch and Update Not Recognized"
    description="Issues with Azure Stack Update Not Recognized"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629272"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-patchandupdate-updatenotrecognized"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Patch and Update Not Recognized

Customers with Azure Stack environments connected to the internet will automatically see "Update Available" in the Admin Portal. For disconnected customers, update release notifications are available vis RSS feed at [Support Content Updates](https://support.microsoft.com/help/4089498/support-content-updates). Select Product as *Azure Stack*, and choose ATOM or RSS.

## **Recommended Steps**

1. Check the release notes any known issues for the specific update package, listed under [Update Package Release Cadence](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence)
2. If the update is marked as *Not Recognized*, try manually importing the update package with the [Import and install updates instructions](https://docs.microsoft.com/azure-stack/operator/azure-stack-update-prepare-package?view=azs-1908#import-and-install-updates). If you have already attempted manually importing the update package delete the blob container from your previous attempt before reimporting the package.
3. If a update is still *Not Recognized* after a retry, continue to open a support case

## **Recommended Documents**

* [Azure Stack servicing policy - Recent Update](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence)
* [Manage updates in Azure Stack overview](https://docs.microsoft.com/azure/azure-stack/azure-stack-updates)
* [Monitor updates in Azure Stack using the privileged endpoint](https://docs.microsoft.com/azure/azure-stack/azure-stack-monitor-update)
* [Use REST to get update status](https://docs.microsoft.com/rest/api/azurestack/updates/get#updatestate)
