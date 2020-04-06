<properties
    pageTitle="Azure Stack Patch and Update Failure"
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
    cloudEnvironments="public, Fairfax"
    articleId="azurestack-patchandupdate-updatefailure"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Patch and Update Failures

Each release of Microsoft software updates is bundled as a single update package.  As an Azure Stack operator, you can import, install, and monitor the installation progress of update packages from the Azure Stack administration portal.

* For information regarding information on how to manage updates for Azure Stack, please review [Manage updates in Azure Stack overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-updates#install-updates-and-monitor-progress)
* For information regarding recent releases, release notes on updates and cadence, please review [Update package release cadence](https://docs.microsoft.com/azure-stack/operator/azure-stack-servicing-policy#update-package-release-cadence)
* For more information regarding security updates for Azure Stack, please review [Azure Stack security updates](https://docs.microsoft.com/azure-stack/operator/azure-stack-release-notes-security-updates-1907)

## **Recommended Steps**

1. Review [Release notes](https://docs.microsoft.com/azure-stack/operator/release-notes) and [Known issues](https://docs.microsoft.com/azure-stack/operator/known-issues) for the update you are applying (choose from the Version drop-down menu)
2. Perform the steps in the [checklist for preparing to apply Azure Stack update](http://docs.microsoft.com/azure-stack/operator/release-notes-checklist#prepare-for-azure-stack-update)
3. For ongoing updates, you can manage, monitor, and resume the progress of the update with the steps in the [checklist during Azure Stack update](https://docs.microsoft.com/azure-stack/operator/release-notes-checklist#during-azure-stack-update)
4. If resuming a previously failed update, run [Test-AzureStack](https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-test) and resolve any identified issues before resuming using steps outlined in [Resume Azure Stack update using PowerShell](https://docs.microsoft.com/azure-stack/operator/azure-stack-monitor-update#resume-a-failed-update-operation)
5. Once the update has completed, follow the steps in the [checklist for after Azure Stack updates](https://docs.microsoft.com/azure-stack/operator/release-notes-checklist#after-azure-stack-update)

## **Recommended Documents**

* [Manage updates in Azure Stack overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-updates#install-updates-and-monitor-progress)<br>
* [Apply updates in Azure Stack](https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates)<br>
* [Update Azure Stack by downloading the package](https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#update-azure-stack-by-downloading-the-package)<br>
* [Import and install updates](https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#import-and-install-updates)<br>
* [Monitor updates in Azure Stack using the privileged endpoint](https://docs.microsoft.com/azure-stack/operator/azure-stack-monitor-update)<br>
* [Test-AzureStack](https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-test)<br>
* [Resume Azure Stack update using PowerShell](https://docs.microsoft.com/azure-stack/operator/azure-stack-monitor-update#resume-a-failed-update-operation)
