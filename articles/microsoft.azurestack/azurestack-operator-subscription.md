<properties
    pageTitle="Azure Stack subscriptions"
    description="Issues related to Azure Stack subscriptions"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="TobyTu"
    ms.author="mquian"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629263"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-operator-subscription"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack subscriptions

If you already have a subscription created, review the recommended steps for answers to common support questions. The recommended documents have more background about how to create subscriptions.

## **Recommended Steps**

* To add or remove another Owner to a subscription, you need to sign in as an Owner of the subscription. For more information, see [Manage access to resources in Azure Stack Hub with role-based access control](https://docs.microsoft.com/azure-stack/user/azure-stack-manage-permissions).
* Here are three ways for an operator to see resource allocations in a tenant's Azure AD:

  * Use the [Get-AzsSubscriberUsage Rest API](https://docs.microsoft.com/powershell/module/azs.commerce.admin/get-azssubscriberusage?view=azurestackps-1.7.2). You can use the [Usage PowerShell script](https://github.com/Azure/AzureStack-Tools/blob/master/Usage/Usagesummary.ps1) from the AzureStack-Tools to easily export the data in a CSV file .
  * Obtain the necessary permissions in the tenant's Azure AD.
  * Lastly, Microsoft support can manually extract information such as VM Compute allocations from Azure Stack Hub.

* As a cloud operator, you can create a subscription for a user from within the administrator portal. Subscriptions you create can be for both public and private offers. For more information, see [Create a subscription as a cloud operator](https://docs.microsoft.com/azure-stack/operator/azure-stack-subscribe-plan-provision-vm#create-a-subscription-as-a-cloud-operator).
* As a tenant user, you can subscribe to a public offer by using the User portal or [New-AzsUserSubscription](https://docs.microsoft.com/powershell/module/azs.subscriptions.admin/new-azsusersubscription?view=azurestackps-1.8.1). For more information, see [Create a subscription as a user](https://docs.microsoft.com/azure-stack/operator/azure-stack-subscribe-plan-provision-vm#create-a-subscription-as-a-user).

## **Recommended Documents**

* [Overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-plan-offer-quota-overview)
* [Offers](https://docs.microsoft.com/azure-stack/operator/azure-stack-plan-offer-quota-overview#offers)
* [Plans](https://docs.microsoft.com/azure-stack/operator/azure-stack-create-plan)
* [Subscriptions](https://docs.microsoft.com/azure-stack/operator/azure-stack-plan-offer-quota-overview#subscriptions)
