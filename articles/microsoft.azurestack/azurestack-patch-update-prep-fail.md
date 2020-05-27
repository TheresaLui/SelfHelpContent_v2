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

<!--- Nick Meader said Peter was considering adding a progress indicator to help customers who are simply waiting for a long-running update to complete. Ning to follow up on status of that work - may be worth mentioning here when available.--->


## **Recommended Steps**

1. This may be caused by the Update Resource Provider (URP) not properly transferring the files from the storage container to an internal infrastructure share for processing:

	* Work around this issue by clicking **Update now** again (not **Resume**). The URP then cleans up the files from the previous attempt and restarts the download.
	* If the problem persists, [manually upload the update package](https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#install-updates-and-monitor-progress)

2. On a weak internet connection, it can also be quicker to [manually upload the package](https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#install-updates-and-monitor-progress)

## **Recommended Documents**

* [2002 Update Process](https://docs.microsoft.com/azure-stack/operator/known-issues#2002-update-process)<br>
* [PreparationFailed](https://docs.microsoft.com/azure-stack/operator/azure-stack-updates-troubleshoot#preparationfailed)<br>
* [Install updates and monitor progress](https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#install-updates-and-monitor-progress)
