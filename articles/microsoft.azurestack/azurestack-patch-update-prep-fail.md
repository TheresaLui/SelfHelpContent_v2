<properties
    pageTitle="Patch and Update - Preparation Failure"
    description="Steps to correct a 'PreparationFailed' error while installing the Azure Stack update."
    service="microsoft.azurestack"
    resource="azurestack"
    authors="v-miegge"
    ms.author="mquian"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32688665"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="17bfc48c-c3f7-4286-bda1-892f299ae748"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Patch and Update - Preparation Failure

When attempting to install the Azure Stack update, the status for the update might fail and change state to **PreparationFailed**.

## **Recommended Steps**

1. This may be caused by the Update Resource Provider (URP) not properly transferring the files from the storage container to an internal infrastructure share for processing:

   Starting with version 1901 (1.1901.0.95), work around this issue by clicking **Update now** again (not **Resume**). The URP then cleans up the files from the previous attempt and restarts the download.

   If the problem persists, manually upload the update package by following the [Install updates](https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#install-updates-and-monitor-progress) section.

2. For internet-connected systems this is usually indicative of the update package being unable to download properly due to a weak internet connection:

   Work around this issue by clicking **Install now** again. If the problem persists, manually upload the update package by following the [Install updates](https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#install-updates-and-monitor-progress) section.

## **Recommended Documents**

* [1908 Update Process](https://docs.microsoft.com/azure-stack/operator/known-issues#1908-update-process)<br>
* [PreparationFailed](https://docs.microsoft.com/azure-stack/operator/azure-stack-updates-troubleshoot#preparationfailed)<br>
* [Install updates and monitor progress](https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#install-updates-and-monitor-progress)
