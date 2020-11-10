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

**Known Issue**

If the **Access Control (IAM)** blade displays **Loading** in a loop, and you can't add new roles to the subscription, make sure that the subscription is checked in the **Directory + Subscription** menu. The menu can be accessed from the top of the portal, near the **Notifications** button, or via the shortcut on the **All resources** blade that displays **Don't see a subscription? Open Directory + Subscription settings**. The subscription must be selected in this menu. This issue affects Azure Stack Hub beginning with version 1910 and will be fixed in an upcoming release.

## **Recommended Steps**

If you already created a subscription, review these answers to common support questions. The recommended documents have more background about how to create subscriptions.

* To add or remove another Owner to a subscription, you need to sign in as an Owner of the subscription. For more information, see [Manage access to resources in Azure Stack Hub with role-based access control](https://docs.microsoft.com/azure-stack/user/azure-stack-manage-permissions).
* Here are three ways for an operator to see resource allocations in a tenant's Azure AD:

  * Use the [Get-AzsSubscriberUsage Rest API](https://docs.microsoft.com/powershell/module/azs.commerce.admin/get-azssubscriberusage?view=azurestackps-1.7.2). You can use the [Usage PowerShell script](https://github.com/Azure/AzureStack-Tools/blob/master/Usage/Usagesummary.ps1) from the AzureStack-Tools to easily export the data in a CSV file.
  * Obtain the necessary permissions in the tenant's Azure AD
  * If necessary, Microsoft support can manually extract information such as VM Compute allocations from Azure Stack Hub

## **Recommended Documents**

* [Overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-plan-offer-quota-overview)
* [Offers](https://docs.microsoft.com/azure-stack/operator/azure-stack-plan-offer-quota-overview#offers)
* [Plans](https://docs.microsoft.com/azure-stack/operator/azure-stack-create-plan)
* [Create a subscription in the portal](https://docs.microsoft.com/azure-stack/operator/azure-stack-subscribe-plan-provision-vm#create-a-subscription-as-a-user)
* [Create a subscription with New-AzsUserSubscription](https://docs.microsoft.com/powershell/module/azs.subscriptions.admin/new-azsusersubscription?view=azurestackps-1.8.1)
