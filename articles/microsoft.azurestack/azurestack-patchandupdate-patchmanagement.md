<properties
    pageTitle="Azure Stack Patch management questions (not related to precheck)"
    description="Assist customers before and during patch and update runs"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT, v-miegge"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32663933"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax"
    articleId="662f64b1-781e-4263-80c2-a6b8ff6e3fe7"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Patch and Update Management

## Availability of Updates

Customers with Azure Stack environments connected to the internet will automatically see "Update Available" in the Admin Portal. For disconnected customers, update release notifications are available via an RSS feed at [Support Content Updates](https://support.microsoft.com/help/4089498/support-content-updates). Select the Product as *Azure Stack*, then choose either ATOM or RSS.

When planning for your maintenance window, it's important to review the specific type of update package released from Microsoft as called out in the respective release note. Aside from the occasional Hotfix, each update package will have a corresponding type, Full or Express. Full update packages update the physical host operating systems in the scale unit and require a larger maintenance window. Express update packages are scoped, and do not update the underlying physical host operating systems [Manage updates in Azure Stack overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-updates). 

Latest update available 1907, an express package.

## **Recommended Steps**

1. [Prepare for Azure Stack update](https://docs.microsoft.com/azure-stack/operator/azure-stack-release-notes-checklist#prepare-for-azure-stack-update)
1. [During Azure Stack update](https://docs.microsoft.com/azure-stack/operator/azure-stack-release-notes-checklist#during-azure-stack-update)
1. [After Azure Stack Update](https://docs.microsoft.com/azure-stack/operator/azure-stack-release-notes-checklist#after-azure-stack-update)
1. Check [Test-AzureStack](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test) and resolve any identified issues before resuming the failed update using steps to [resume Azure Stack update using PowerShell](https://docs.microsoft.com/azure/azure-stack/azure-stack-monitor-update#resume-a-failed-update-operation)

For detailed information on recent releases, release notes on updates and cadence, please review [Update package release cadence](https://docs.microsoft.com/azure-stack/operator/azure-stack-servicing-policy#update-package-release-cadence).

## **Recommended Documents**

* [Manage updates in Azure Stack overview](https://docs.microsoft.com/azure/azure-stack/azure-stack-updates)<br>
* [Monitor updates in Azure Stack using the privileged endpoint](https://docs.microsoft.com/azure/azure-stack/azure-stack-monitor-update)<br>
* [Integrate external monitoring solution with Azure Stack - Integrate with Operations Manager](https://docs.microsoft.com/azure-stack/operator/azure-stack-integrate-monitor?view=azs-1908#integrate-with-operations-manager)
