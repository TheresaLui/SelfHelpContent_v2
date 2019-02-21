<properties
    pageTitle="Azure Stack tenant and admin portal impact for 1811 update"
    description="Advise customers of portal impact while applying 1811 update"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629244, 32629245"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
	articleId="88df065c-0dc6-4e81-b7e9-7c45e10b8857"
/>

# Azure Stack Tenant and Admin Portal Impact for 1811 Update

### **Important note about portal impact during 1811 update**

The Azure Stack 1811 update contains a new [extension host](https://docs.microsoft.com/azure/azure-stack/azure-stack-extension-host-prepare) that secures external endpoints published by Azure Stack. Prior to installing 1811 update, all instances of Azure Stack Administrator portals **must be closed** or the **install will fail**. 

While installing the 1811 update, the Azure Stack user portal is unavailable while the extension host is configured. This can take up to 5 hours. During that time, you can check the status of an update, or resume a failed update installation using [Azure Stack Administrator PowerShell or the privileged endpoint](https://docs.microsoft.com/azure/azure-stack/azure-stack-monitor-update#use-the-update-management-cmdlets).

## **Recommended Documents**

* See the 1811 Update Release Notes listed under [Recent Updates](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence)
* [Prepare for extension host for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-extension-host-prepare)
* [Monitor updates in Azure Stack using the privileged endpoint](https://docs.microsoft.com/azure/azure-stack/azure-stack-monitor-update#use-the-update-management-cmdlets)
