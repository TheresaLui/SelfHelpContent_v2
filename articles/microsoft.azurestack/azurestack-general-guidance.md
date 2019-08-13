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
    cloudEnvironments="public"
    articleId="azurestack-general-guidance"
/>

# Azure Stack General Guidance

The recommended steps below may help solve or isolate the issue. If the steps below help identify a specific issue, please go back and select the specific problem type, as it may have specific documentation on the issue or will help us work with you in resolving the issue. 

## **Recommended Steps**

1. Review [troubleshooting known issues](https://docs.microsoft.com/azure/azure-stack/azure-stack-troubleshooting) and [release notes for most recent updates](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence)
1. Perform [validation for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test) using the Test-AzureStack cmdlet
1. Review the available updates:  [Manage updates in Azure Stack overview](https://docs.microsoft.com/azure/azure-stack/azure-stack-updates) and [Update package release cadence](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence)
1. Use [log collection tool](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostics) to collect traces and log files

## **Recommended Documents**

### Buying Azure Stack considerations

* [How to buy](https://azure.microsoft.com/overview/azure-stack/how-to-buy/)
* [Azure Stack Overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-overview)
* [What is the Azure Stack Development Kit](https://docs.microsoft.com/azure-stack/asdk/asdk-what-is)

### ASDK

Thank you for your interest in Azure Stack. As outlined in Microsoft Azure Stack Troubleshooting, the Azure Stack Development Kit is offered as an evaluation environment with no support available through Microsoft Customer Support Services. Please understand that any support cases opened for ASDK will be redirected to the MSDN Forum and closed.

### Validate, Diagnose and Update Cadence

* [How to Diagnostics in Azure Stack](https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostics)<br>
* [How to Validate Azure Stack system state](https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-test)<br>
* [Update Package Release cadence](https://docs.microsoft.com/azure-stack/operator/azure-stack-servicing-policy#update-package-release-cadence)

### Supported Operating System and VM Sizes

* [Guess Operating System supported on Azure Stack](https://docs.microsoft.com/azure-stack/operator/azure-stack-supported-os)
* [VM Sizes supported in Azure Stack](https://docs.microsoft.com/azure-stack/user/azure-stack-vm-sizes)

### Azure Marketplace
* [Azure Marketplace items available for Azure Stack](https://docs.microsoft.com/azure-stack/operator/azure-stack-marketplace-azure-items)

### Manage Capacity

#### Memory

To increase the total available memory capacity for Azure Stack, you can add additional memory. In Azure Stack, your physical server is also referred to as a scale unit node. All scale unit nodes that are members of a single scale unit must have [the same amount of memory](https://docs.microsoft.com/azure-stack/operator/azure-stack-manage-storage-physical-memory-capacity).

#### Rentention Period

The retention period setting allows a cloud operator to specify a time period in days (between 0 and 9999 days) during which any deleted account can potentially be recovered. The default retention period is set to 0 days. Setting the value to "0" means that any deleted account is immediately out of retention and marked for periodic garbage collection.

* [Set the retention period](https://docs.microsoft.com/azure-stack/operator/azure-stack-manage-storage-accounts#set-the-retention-period)

### Security, compliance & Identity  

#### Manage RBAC

A user in Azure Stack can be a reader, owner, or contributor for each instance of a subscription, resource group, or service.

* [Azure Stack Manage RBAC](https://docs.microsoft.com/azure-stack/operator/azure-stack-manage-permissions)

If the built-in roles for Azure resources don't meet the specific needs of your organization, you can create your own custom roles. For this tutorial, you create a custom role named Reader Support Tickets using Azure PowerShell.

* [Tutorial: Create a custom role for Azure resources using Azure PoweShell](https://docs.microsoft.com/azure/role-based-access-control/tutorial-custom-role-powershell)<br>
* [Manage usage and billing as a CSP](https://docs.microsoft.com/azure-stack/operator/azure-stack-add-manage-billing-as-a-csp#create-a-csp-or-apss-subscription)

### Manage usage and billing as a CSP

[Create a CSP or APSS Subscription](https://docs.microsoft.com/en-us/azure-stack/operator/azure-stack-add-manage-billing-as-a-csp#create-a-csp-or-apss-subscription)

Choose the type of shared services account that you use for Azure Stack. The types of subscriptions that can be used for registration of a multi-tenant Azure Stack are:

* Cloud Service Provider<br>
* Partner Shared Services subscription
