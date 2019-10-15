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
    cloudEnvironments="public"
    articleId="azurestack-patchandupdate-updatefailure"
/>

# Azure Stack Patch and Update Failures

Each release of Microsoft software updates is bundled as a single update package.  As an Azure Stack operator, you can import, install, and monitor the installation progress of update packages from the Azure Stack administration portal.

* For information regarding information on how to manage updates for Azure Stack, please review [Manage updates in Azure Stack overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-updates#install-updates-and-monitor-progress)
* For information regarding recent releases, release notes on updates and cadence, please review [Update package release cadence](https://docs.microsoft.com/azure-stack/operator/azure-stack-servicing-policy#update-package-release-cadence)
* For more information regarding security updates for Azure Stack, please review [Azure Stack security updates](https://docs.microsoft.com/azure-stack/operator/azure-stack-release-notes-security-updates-1907).

## **Recommended Steps**

1. For ongoing updates, you can monitor the progress of the update with the instructions outlined in [Monitor updates in Azure Stack](https://docs.microsoft.com/azure-stack/operator/azure-stack-update-monitor)
2. Review all known issues regarding Update specific issues:

    * [1907 Known issues](https://docs.microsoft.com/azure-stack/operator/azure-stack-release-notes-known-issues-1907) and [1907 Update process](https://docs.microsoft.com/azure-stack/operator/azure-stack-release-notes-known-issues-1907#update-process)<br>
    * [1906 Known issues](https://docs.microsoft.com/azure-stack/operator/azure-stack-release-notes-known-issues-1906) and [1906 Update process](https://docs.microsoft.com/azure-stack/operator/azure-stack-release-notes-known-issues-1906#update-process)<br>
    * [1905 Known issues](https://docs.microsoft.com/azure-stack/operator/azure-stack-release-notes-known-issues-1905) and [1905 Update process](https://docs.microsoft.com/azure-stack/operator/azure-stack-release-notes-known-issues-1905#update-process)<br>
    * [1904 Known issues](https://docs.microsoft.com/azure-stack/operator/azure-stack-release-notes-known-issues-1904) and [1904 Update process](https://docs.microsoft.com/azure-stack/operator/azure-stack-release-notes-known-issues-1904#update-process)

3. Review the checklist for [update-related activities for Azure Stack operators](https://docs.microsoft.com/azure-stack/operator/azure-stack-release-notes-checklist#during-azure-stack-update) when preparing to apply an update to Azure Stack
4. If resuming a previously failed update, run [Test-AzureStack](https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-test) and resolve any identified issues before resuming using steps outlined in [Resume Azure Stack update using PowerShell](https://docs.microsoft.com/azure-stack/operator/azure-stack-monitor-update#resume-a-failed-update-operation)

## **Recommended Documents**

* [Manage updates in Azure Stack overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-updates#install-updates-and-monitor-progress)<br>
* [Apply updates in Azure Stack](https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates)<br>
* [Update Azure Stack by downloading the package](https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#update-azure-stack-by-downloading-the-package)<br>
* [Import and install updates](https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#import-and-install-updates)<br>
* [Monitor updates in Azure Stack using the privileged endpoint](https://docs.microsoft.com/azure-stack/operator/azure-stack-monitor-update)<br>
* [Test-AzureStack](https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-test)<br>
* [Resume Azure Stack update using PowerShell](https://docs.microsoft.com/azure-stack/operator/azure-stack-monitor-update#resume-a-failed-update-operation)
