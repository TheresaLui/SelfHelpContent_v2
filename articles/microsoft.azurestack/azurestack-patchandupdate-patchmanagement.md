<properties
    pageTitle="Azure Stack Patch and Update Management"
    description="Assist customers before and during patch and update runs"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629180,32629240,32630577"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
	articleId="662f64b1-781e-4263-80c2-a6b8ff6e3fe7"
/>

# Azure Stack Patch and Update Management

### **Important note about portal impact during 1811 update**

The Azure Stack 1811 update contains a new [extension host](https://docs.microsoft.com/azure/azure-stack/azure-stack-extension-host-prepare) that secures external endpoints published by Azure Stack. Prior to installing 1811 update, all instances of Azure Stack Administrator portals **must be closed** or the **install will fail**. 

While installing the 1811 update, the Azure Stack user portal is unavailable while the extension host is configured. This can take up to 5 hours. During that time, you can check the status of an update, or resume a failed update installation using [Azure Stack Administrator PowerShell or the privileged endpoint](https://docs.microsoft.com/azure/azure-stack/azure-stack-monitor-update#use-the-update-management-cmdlets).

### **Availability of Updates:**

Customers with Azure Stack environments connected to the internet will automatically see "Update Available" in the Admin Portal. For disconnected customers, update release notifications are available vis RSS feed at [Support Content Updates](https://support.microsoft.com/help/4089498/support-content-updates). Select Product as *Azure Stack*, and choose ATOM or RSS.

### **If you are preparing to apply an Azure Stack update:**

1. Check the release notes for the specific update package, listed under [Update Package Release Cadence](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence)
2. Perform a pre-check on the health of your environment by running Test-AzureStack according to the steps under [Plan for Updates](https://docs.microsoft.com/azure/azure-stack/azure-stack-updates#plan-for-updates)
3. Resolve any operational issues found in Test-AzureStack output, including all warnings and failures. Also review active alerts and resolve any that require action.

### **If you are monitoring an ongoing update:**

1. Check the status of the update using the steps to [Monitor updates in Azure Stack using the privileged endpoint](https://docs.microsoft.com/azure/azure-stack/azure-stack-monitor-update#use-the-update-management-cmdlets)

## **Recommended Documents**

* [Azure Stack servicing policy - Recent Update](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence)
* [Manage updates in Azure Stack overview](https://docs.microsoft.com/azure/azure-stack/azure-stack-updates)
* [Monitor updates in Azure Stack using the privileged endpoint](https://docs.microsoft.com/azure/azure-stack/azure-stack-monitor-update)
