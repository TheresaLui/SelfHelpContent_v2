<properties
	pageTitle="how to move services to another subscription"
	description="how to move services to another subscription"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32632956"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="public"
	articleId="accessandresourcemanagementmoveservicestoanothersubscription"
/>

# how to move services to another subscription

## **Recommended Steps**

Azure resources can be moved to either another Azure subscription or another resource group under the same subscription. You can use the Azure portal, Azure PowerShell, Azure CLI, or the REST API to [move resources](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources).<br>

### Move resources

* [Tutorial: Move Azure resources to another resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-tutorial-move-resources)<br>
* [Services that can be moved](https://docs.microsoft.com/azure/azure-resource-manager/move-support-resources)<br>
 
_Note:_ If you want to upgrade your Azure subscription (such as switching from free to pay-as-you-go), you need to convert your subscription.<br>

  * To upgrade a free trial, see [Upgrade your Free Trial or Microsoft Imagine Azure subscription to Pay-As-You-Go](https://docs.microsoft.com/azure/billing/billing-upgrade-azure-subscription)
  * To change a pay-as-you-go account, see [Change your Azure Pay-As-You-Go subscription to a different offer](https://docs.microsoft.com/azure/billing/billing-how-to-switch-azure-offer)
  * If you can't convert the subscription, [create an Azure support request](https://docs.microsoft.com/azure/azure-supportability/how-to-create-azure-support-request). Select Subscription Management for the issue type.

### Add or Associate an Azure subscription to your Azure Active Directory tenant

  1. Sign in and select the subscription you want to use from the [Subscriptions page in Azure portal](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade)
  2. Select **Change directory**
  3. Review any warnings that appear, and then select **Change**
  4. The directory is changed for the subscription and you get a success message
  5. Use the Directory switcher to go to your new directory. _Note:_ It might take up to 10 minutes for everything to show up properly.<br>

### EA Subscriptions

* [How to create EA Subscriptions](https://docs.microsoft.com/azure/azure-resource-manager/programmatically-create-subscription?tabs=rest)<br>
* [Grant access to create EA Subscriptions](https://docs.microsoft.com/azure/azure-resource-manager/grant-access-to-create-subscription?tabs=rest)<br>

## **Recommended Documents**

* [Access Azure Active Directory to create a new tenant](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-access-create-new-tenant)
* [How to assign directory roles to users with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal)
* [Transferring ownership of an Azure subscription](https://docs.microsoft.com/azure/billing-subscription-transfer)
* [Move resources to new resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)
* [Manage resources using Azure portal](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-portal)
* [Associate or add an Azure subscription Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-how-subscriptions-associated-directory)<br>
