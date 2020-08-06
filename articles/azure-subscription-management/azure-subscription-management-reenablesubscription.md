<properties
	pageTitle="reenable subscriptions"
	description="reenable subscriptions"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32632954"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="reenablesubscriptions"
	ownershipId="ASMS_SubscriptionManagement"
/>

# Re enable Subscription

Your Azure subscription can get disabled because your credit has expired, you reached your spending limit, have an overdue bill, hit your credit card limit, or because the subscription was cancelled by the Account Administrator. Refer below on how you can re-enable your subscription 
Learn more: [Reactivate Azure subscription](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable)

## **Recommended Steps**

**Re-enable your Azure Subscription (subscription was accidentally cancelled)** <br>
The [Account Administrator](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#whoisaa) can reactivate a cancelled Pay-As-You-Go subscription in the Account Center

1. Sign in to the [Account Center](https://account.windowsazure.com/Subscriptions)
2. Select the cancelled subscription. Click **Reactivate**
3. For other subscription types, [contact support](https://portal.azure.com/?#blade/Microsoft_Azure_Support/HelpAndSupportBlade) to have your subscription reactivated

### **Expired credit card**
When you sign up for an **Azure free account**, you get a Free Trial subscription, which provides you $200 in Azure credits for 30 days and 12 months of free services. At the end of 30 days, Azure disables your subscription. Your subscription is disabled to protect you from accidentally incurring charges for usage beyond the credit and free services included with your subscription. To continue using Azure services, you must [upgrade your subscription](https://docs.microsoft.com/azure/billing/billing-upgrade-azure-subscription). After you upgrade, your subscription still has access to free services for 12 months. You only get charged for usage beyond the free services and quantities.<br>
Learn more: [Expired credit card](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable#your-credit-is-expired)

### **Spending Limit reached**
When your usage reaches the spending limit, Azure disables your subscription for the remainder of that billing period. Your subscription is disabled to protect you from accidentally incurring charges for usage beyond the credit included with your subscription. To remove your spending limit, see [Azure spending limit](https://docs.microsoft.com/azure/cost-management-billing/manage/spending-limit).<br>
Learn more: [Reached your spending limit](https://docs.microsoft.com/azure/cost-management-billing/manage/subscription-disabled#you-reached-your-spending-limit)

### **Bill past due**
To resolve past due balance, see [Resolve past due balance for your Azure subscription after getting an email from Azure](https://docs.microsoft.com/azure/billing/billing-azure-subscription-past-due-balance)

### **Bill exceeds your credit card limit**
To resolve this issue, [switch to a different credit card](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card). Or if you're representing a business, you can [switch to pay by invoice](https://docs.microsoft.com/azure/billing/billing-how-to-pay-by-invoice).<br>

**Note**: A new Subscription Anniversary (SA) date will be assigned to subscriptions that have been re-enabled. The number of days (interval) in which the subscription was suspended, will be added to the original SA date. Any Anniversary date falling on the 29th, 30th, or 31st will result in the SA date being set to the 1st of the following month.<br>
Example:

  * Your original Subscription Anniversary is the 25th
  * The subscription was suspended on 10/3 and re-enabled on 10/9
  * The subscription was disabled for 6 days (interval of 6)
  * The interval is then added to the original SA, and the sum becomes the new SA date (25+6=31).
**Note**: In this example, since the SA date is now greater than 28, the new SA date will be the 1st of the following month.

## **Recommended Documents**

* [Switch subscription](https://docs.microsoft.com/azure/billing/billing-how-to-switch-azure-offer)
* [Cancel subscription](https://docs.microsoft.com/azure/billing/billing-how-to-cancel-azure-subscription)
* [Azure Marketplace](https://azuremarketplace.microsoft.com/marketplace/?source=datamarket)
* [How to download your invoice and usage data](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date)
* [How to request copy of Azure invoice via email](https://azure.microsoft.com/blog/azure-email-invoices/)
* [Migrate resources between accounts/subscriptions](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)
* [Add/Manage admins and co-admins](https://docs.microsoft.com/azure/billing/billing-add-change-azure-subscription-administrator)
* Locate the [Account Admin](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#whoisaa)
* [What do I do if my Azure subscription becomes disabled? ](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable/)
* [Azure spending limit](https://docs.microsoft.com/azure/cost-management-billing/manage/spending-limit)
