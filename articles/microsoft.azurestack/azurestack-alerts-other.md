<properties
    pageTitle="Azure Stack Hub alerts"
    description="Azure Stack Hub alerts that are not covered by other specific alert topics"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629237"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-alerts-other"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Hub Alerts

**Common Issues**

After applying the 2002 update, you might see a false-positive alert in the Administrator portal for an **Invalid Time Source**. The alert can be ignored and will be fixed in an upcoming release. For more information, see [Azure Stack Hub known issues](https://docs.microsoft.com/azure-stack/operator/known-issues?view=azs-2002).  

If you see Usage Bridge alert **AADSTS900439: Confidential Client requests are not supported** or **certificateValidationError**, the simplest solution is to [re-register Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-registration). Make sure you are using correct [endpoints](https://docs.microsoft.com/azure-stack/operator/azure-stack-integrate-endpoints) to register.  

**NOTE**: Before you create a support ticket, review [**Release notes**](https://docs.microsoft.com/azure-stack/operator/release-notes) and [**Known issues**](https://docs.microsoft.com/azure-stack/operator/known-issues) for the update you are applying (choose from the Version drop-down menu). This may save you time and effort.

## **Recommended Steps**

A critical alert should be addressed urgently because it can impact users. Please attempt the remediation steps in the alert before opening a case. In some alerts, you can select **Repair** in the Remediation details of the alert to resolve the issue. You can run **Repair** again if it fails. 

## **Recommended Documents**

* [Monitor health and alerts in Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-monitor-health?view=azs-2002)


