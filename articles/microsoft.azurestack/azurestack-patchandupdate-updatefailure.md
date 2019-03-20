<properties
    pageTitle="Azure Stack Patch and Update Failure"
    description="Assist customers before and during patch and update runs"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
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

## **Recommended Steps**

1. Check the status of the update using the steps to [monitor updates in Azure Stack using the privileged endpoint](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-monitor-update#get-high-level-status-of-the-current-update-run)
2. If the update fails, check for known issues in [Release Notes for the update your are applying](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence)
3. Check [Test-AzureStack](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test) and resolve any identified issues before resuming the failed update using steps to [resume Azure Stack update using PowerShell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-monitor-update#resume-a-failed-update-operation)
4. If retrying the update still does not work, continue to open a support case

## **Recommended Documents**

* [Azure Stack Recent Updates and Release Notes](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence)
* [Manage updates in Azure Stack overview](https://docs.microsoft.com/azure/azure-stack/azure-stack-updates)
* [Monitor updates in Azure Stack using the privileged endpoint](https://docs.microsoft.com/azure/azure-stack/azure-stack-monitor-update)