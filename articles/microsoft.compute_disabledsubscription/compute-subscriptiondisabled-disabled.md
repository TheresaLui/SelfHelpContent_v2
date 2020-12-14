<properties
	pageTitle="Subscription Disabled RCA"
	description="RCA - Subscription Disabled"
	infoBubbleText="Subscription disabled. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="Compute-SubscriptionDisabledInformation-Disabled"
	diagnosticScenario="SubscriptionStatesInsight"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We detected that the subscription **<!--$subscription-->SubscriptionID<!--/$subscription-->** was recently disabled on **<!--$lastdisabledtime-->lastdisabledtime<!--/$lastdisabledtime--> (UTC)**. Resources for this subscription and operations on those resources may be impacted. Use the following guidance to re-enable your subscription.
<!--/issueDescription-->

Your Azure subscription can be disabled because your credit card has expired, you reached your spending limit, have an overdue bill, reached your credit card limit, or because the subscription was cancelled by the Account Administrator. 

[Learn more](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable)

## **Recommended Steps**

**Re-enable your Azure Subscription (subscription was accidentally cancelled)** <br>

The [Account Administrator](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#whoisaa) can reactivate a cancelled Pay-As-You-Go subscription in the Account Center:

1. Sign in to the [Account Center](https://account.windowsazure.com/Subscriptions)
2. Select the cancelled subscription. Click **Reactivate**
3. For other subscription types, [contact support](https://portal.azure.com/?#blade/Microsoft_Azure_Support/HelpAndSupportBlade) to have your subscription reactivated

### **Expired credit card**

When you sign up for an **Azure free account**, you receive a free trial subscription, which provides you with $200 in Azure credits for 30 days and 12 months of free services. At the end of 30 days, Azure disables your subscription. Your subscription is disabled to protect you from accidentally incurring charges for usage beyond the credit and beyond the free services included with your subscription. 

To continue using Azure services, you must [upgrade your subscription](https://docs.microsoft.com/azure/billing/billing-upgrade-azure-subscription). After you upgrade, your subscription still has access to free services for 12 months. You will be charged only for usage beyond the free services and quantities.<br>

[Learn more](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable#your-credit-is-expired).

### **Spending limit reached**

When your usage reaches the spending limit, Azure disables your subscription for the remainder of that billing period. Your subscription is disabled to protect you from accidentally incurring charges for usage beyond the credit included with your subscription. To remove your spending limit, see [Azure spending limit](https://docs.microsoft.com/azure/cost-management-billing/manage/spending-limit).<br>

[Learn more](https://docs.microsoft.com/azure/cost-management-billing/manage/subscription-disabled#you-reached-your-spending-limit).

### **Bill is past due**

To resolve a past-due balance, see [resolve past due balance for your Azure subscription after getting an email from Azure](https://docs.microsoft.com/azure/billing/billing-azure-subscription-past-due-balance).

### **Bill exceeds your credit card limit**

To resolve this issue, [switch to a different credit card](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card). Or if you're representing a business, you can [switch to pay by invoice](https://docs.microsoft.com/azure/billing/billing-how-to-pay-by-invoice).<br>

## **Recommended Documents**

* [What do I do if my Azure subscription becomes disabled?](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable/)
* [Switch subscription](https://docs.microsoft.com/azure/billing/billing-how-to-switch-azure-offer)
* [Cancel subscription](https://docs.microsoft.com/azure/billing/billing-how-to-cancel-azure-subscription)
* [Azure Marketplace](https://azuremarketplace.microsoft.com/marketplace/?source=datamarket)
* [How to download your invoice and usage data](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date)
* [How to request copy of Azure invoice via email](https://azure.microsoft.com/blog/azure-email-invoices/)
* [Migrate resources between accounts/subscriptions](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)
* [Add/Manage admins and co-admins](https://docs.microsoft.com/azure/billing/billing-add-change-azure-subscription-administrator)
* Locate the [Account Admin](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#whoisaa)
* [Azure spending limit](https://docs.microsoft.com/azure/cost-management-billing/manage/spending-limit)
