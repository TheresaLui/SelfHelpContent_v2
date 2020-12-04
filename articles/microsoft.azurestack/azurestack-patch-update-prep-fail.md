<properties
  pagetitle="Patch and Update - Preparation Failure"
  service="microsoft.azurestack"
  resource="azurestack"
  ms.author="mquian,patricka"
  selfhelptype="Generic"
  supporttopicids="32688665"
  resourcetags=""
  productpesids="16226"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="17bfc48c-c3f7-4286-bda1-892f299ae748"
  ownershipid="StorageMediaEdge_AzureStack_Hub" />
# Patch and Update - Preparation Failure

When attempting to install the Azure Stack update, the status for the update might fail and change state to **PreparationFailed**.

<!--- Nick Meader said Peter was considering adding a progress indicator to help customers who are simply waiting for a long-running update to complete. Ning to follow up on status of that work - mayazure-stack-update-prepare-package be worth mentioning here when available.--->


## **Recommended Steps**

1. This may be caused by the Update Resource Provider (URP) not properly transferring the files from the storage container to an internal infrastructure share for processing:

	* Work around this issue by clicking **Update now** again (not **Resume**). The URP then cleans up the files from the previous attempt and restarts the download.
	* If the problem persists, manually download, import, and install the update package. For more information, see [Prepare an Azure Stack Hub update package](https://docs.microsoft.com/azure-stack/operator/azure-stack-update-prepare-package).

2. On a weak internet connection, it can be quicker to [manually upload the package](https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#install-updates-and-monitor-progress)

## **Recommended Documents**

* [2002 Update Process](https://docs.microsoft.com/azure-stack/operator/known-issues#2002-update-process)<br>
* [PreparationFailed](https://docs.microsoft.com/azure-stack/operator/azure-stack-updates-troubleshoot#preparationfailed)<br>
* [Install updates and monitor progress](https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#install-updates-and-monitor-progress)
