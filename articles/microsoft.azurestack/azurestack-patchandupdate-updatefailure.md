<properties
    pageTitle="Azure Stack Hub Patch and Update Failure"
    description="Assist customers during patch and update runs, or after a failure"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT, v-miegge"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629195,32630577"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-patchandupdate-updatefailure"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Hub Patch and Update Failures

<!---this is number one hit topic. This currently is sunny day content. Most customers coming through this path require a break-glass solution. MPI is very high. Some engineering work in 2005 to improve perf of patch and update by using image-based process. Look for how to streamline.  --->

**NOTE**: Before you create a support ticket, review [**Release notes**](https://docs.microsoft.com/azure-stack/operator/release-notes) and [**Known issues**](https://docs.microsoft.com/azure-stack/operator/known-issues) for the update you are applying (choose from the Version drop-down menu). This may save you time and effort.

Each release of Microsoft software updates is bundled as a single update package. As an Azure Stack Hub operator, you can import, install, and monitor the installation progress of update packages from the Azure Stack Hub Administration portal. 

* For information regarding information on how to manage updates for Azure Stack Hub, please review [Manage updates in Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-updates#install-updates-and-monitor-progress)
* For information regarding recent releases, release notes on updates and cadence, please review [Update package release cadence](https://docs.microsoft.com/azure-stack/operator/azure-stack-servicing-policy#update-package-release-cadence)
* For information regarding security updates for Azure Stack Hub, please review [Azure Stack Hub security updates](https://docs.microsoft.com/azure-stack/operator/release-notes-security-updates)

## **Recommended Steps**

1. Review [Release notes](https://docs.microsoft.com/azure-stack/operator/release-notes) and [Known issues](https://docs.microsoft.com/azure-stack/operator/known-issues) for the update you are applying (choose from the Version drop-down menu)
1. Enable [proactive diagnostic log collection](https://docs.microsoft.com/azure-stack/operator/azure-stack-configure-automatic-diagnostic-log-collection-tzl) to automatically share logs with Microsoft support as needed
2. Perform the steps in the [checklist for preparing to apply Azure Stack Hub update](http://docs.microsoft.com/azure-stack/operator/release-notes-checklist#prepare-for-azure-stack-hub-update)
3. For ongoing updates, you can manage, monitor, and resume the progress of the update with the steps in the [checklist during Azure Stack Hub update](https://docs.microsoft.com/azure-stack/operator/release-notes-checklist#during-azure-stack-hub-update)
4. If resuming a previously failed update, run [Test-AzureStack](https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-test) and resolve any identified issues before resuming using steps outlined in [Resume Azure Stack Hub update using PowerShell](https://docs.microsoft.com/azure-stack/operator/azure-stack-monitor-update#resume-a-failed-update-operation)
5. Once the update has completed, follow the steps in the [checklist for after Azure Stack Hub updates](https://docs.microsoft.com/azure-stack/operator/release-notes-checklist#after-azure-stack-hub-update)


## **Recommended Documents**

* [Manage updates in Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-updates#install-updates-and-monitor-progress)<br>
* [Apply updates in Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates)<br>
* [Update Azure Stack Hub by downloading the package](https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#update-azure-stack-hub-by-downloading-the-package)<br>
* [Import and install updates](https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#import-and-install-updates)<br>
* [Monitor updates in Azure Stack Hub using the privileged endpoint](https://docs.microsoft.com/azure-stack/operator/azure-stack-monitor-update)<br>
* [Test-AzureStack](https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-test)<br>
* [Resume Azure Stack Hub update using PowerShell](https://docs.microsoft.com/azure-stack/operator/azure-stack-monitor-update#resume-a-failed-update-operation)
