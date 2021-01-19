<properties
	pageTitle="reenable subscriptions"
	description="reenable subscriptions"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="lishepar"
	ms.author="lishepar"
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

Your Azure subscription can get disabled because your credit has expired, you reached your spending limit, have an overdue bill, hit your credit card limit, or because the subscription was cancelled by a Service Administrator or Subscription owner. Refer below on how you can re-enable your subscription
Learn more: [Reactivate Azure subscription](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable)

## **Recommended Steps**

**Re-enable your Azure Subscription (subscription was accidentally cancelled)** <br>
If you have permissions, you can reactivate an individual subscription with pay-as-you-go rates in the Azure portal.

1. Sign in to the [Subscriptions page in Azure portal](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade)
2. Go to subscriptions and select the cancelled subscription
3. Click **Reactivate**
4. Confirm reactivation by selecting OK

### **Bill past due**
To resolve past due balance, see [Resolve past due balance for your Azure subscription after getting an email from Azure](https://docs.microsoft.com/azure/billing/billing-azure-subscription-past-due-balance)

**Need to make a payment** <br>
A subscription can be disabled due to a non-payment. To re-enable a subscription, navigate to [invoices](https://portal.azure.com/#blade/Microsoft_Azure_GTM/ModernBillingMenuBlade/Invoices) under billing and select Pay Now to make a one-time payment. For modern customers,avoid missing future payments by navigating to [payment methods](https://portal.azure.com/#blade/Microsoft_Azure_GTM/ModernBillingMenuBlade/billingAccountPaymentMethodItem), select the **Default payment method** and updating your payment information.

Learn more: (How to pay your bill for Microsoft Azure)[https://docs.microsoft.com/en-us/azure/cost-management-billing/understand/pay-bill]
(Pay for your subscription by invoice)[https://docs.microsoft.com/en-us/azure/cost-management-billing/manage/pay-by-invoice]

**Made a payment but subscription is still disabled** <br>
It can take up to 24 hours after a payment has been made for your subscription status to reflect your payment. If it has been longer then 24 hours and your subscription is still disabled, please submit a support request for further assistance.

### **Spending Limit reached**
When your usage reaches the spending limit, Azure disables your subscription for the remainder of that billing period. Your subscription is disabled to protect you from accidentally incurring charges for usage beyond the credit included with your subscription. To remove your spending limit, see [Azure spending limit](https://docs.microsoft.com/azure/cost-management-billing/manage/spending-limit).<br>
Learn more: [Reached your spending limit](https://docs.microsoft.com/azure/cost-management-billing/manage/subscription-disabled#you-reached-your-spending-limit)

### **Bill exceeds your credit card limit**
To resolve this issue, [switch to a different credit card](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card). Or if you're representing a business, you can [switch to pay by invoice](https://docs.microsoft.com/azure/billing/billing-how-to-pay-by-invoice).<br>

**Note**: A new Subscription Anniversary (SA) date will be assigned to subscriptions that have been re-enabled. The number of days (interval) in which the subscription was suspended, will be added to the original SA date. Any Anniversary date falling on the 29th, 30th, or 31st will result in the SA date being set to the 1st of the following month.<br>
Example:

  * Your original Subscription Anniversary is the 25th
  * The subscription was suspended on 10/3 and re-enabled on 10/9
  * The subscription was disabled for 6 days (interval of 6)
  * The interval is then added to the original SA, and the sum becomes the new SA date (25+6=31).
**Note**: In this example, since the SA date is now greater than 28, the new SA date will be the 1st of the following month.

**Tried self-reactivation and failed** <br>
After selecting OK to confirm reactivation, please allow up to 30 minutes for the changes to be reflected in the portal. To check if the subscription is reactivated, refresh the page and check the status of the subscription. If the subscription is still in a disabled state after 30 minutes, please submit a support request for further assistance.

## **Recommended Documents**

* [Reactivate a disabled Azure subscription](https://docs.microsoft.com/azure/cost-management-billing/manage/subscription-disabled)
* [The subscription was accidentally disabled](https://docs.microsoft.com/azure/cost-management-billing/manage/subscription-disabled#the-subscription-was-accidentally-canceled)
* [What do I do if my Azure subscription becomes disabled? ](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable/)
* [Azure spending limit](https://docs.microsoft.com/azure/cost-management-billing/manage/spending-limit)
* [Remove the spending limit in Azure portal](https://docs.microsoft.com/azure/cost-management-billing/manage/spending-limit#remove)
* [My subscription is still disabled after updating the payment method](https://docs.microsoft.com/en-us/azure/cost-management-billing/manage/billing-troubleshoot-azure-payment-issues#my-subscription-is-still-disabled-after-updating-the-payment-method)
