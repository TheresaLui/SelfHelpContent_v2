<properties
    pageTitle="Azure Stack General Guidance"
    description="Azure Stack General Guidance"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT, v-miegge"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629177"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-general-guidance"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack General Guidance

The recommended steps below may help solve or isolate the issue. If the steps below help identify a specific issue, please go back and select the specific problem type, as it may have specific documentation on the issue or will help us work with you in resolving the issue.

## **Recommended Steps**

1. Review [release notes for most recent updates](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence)
1. Perform [validation for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test) using the Test-AzureStack cmdlet
1. Review the available [updates in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-updates) 
1. Use [log collection tool](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostics) to collect traces and log files

## **Recommended Documents**

* For general troubleshooting and topics that cover common questions sent to Microsoft Customer Support Services (CSS), see [Azure Stack Hub Troubleshooting](https://docs.microsoft.com/azure-stack/operator/azure-stack-troubleshooting). For more details about specific concepts and tasks, see the [Azure Stack Operator Documnentation](https://docs.microsoft.com/azure-stack/operator).
* For guidance on setting up tools to work with Azure Stack Hub, you can find instructions for using [PowerShell](https://docs.microsoft.com/azure-stack/operator/powershell-install-az-module) or [Azure CLI](https://docs.microsoft.com/azure-stack/user/azure-stack-version-profiles-azurecli2).
* With PowerShell installed on your management machine, you can connect to your Azure Stack Hub environment. For instruction see [Connect to Azure Stack Hub with PowerShell](https://docs.microsoft.com/azure-stack/operator/azure-stack-powershell-configure-admin).
* For an overview of Azure Stack Hub, see [Azure Stack Hub overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-overview).
* To learn about Azure Stack Hub Marketplace, see [Azure Stack Hub Marketplace overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-marketplace?view=azs-1910) or [Add Azure Kubernetes Services engine prerequisites to Azure Stack Hub Marketplace](https://docs.microsoft.com/azure-stack/operator/azure-stack-aks-engine?view=azs-1910).
