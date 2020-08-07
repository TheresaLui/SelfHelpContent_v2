<properties
	pageTitle="Pricing-I have questions about my spending limits"
	description="Pricing-I have questions about my spending limits"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32632938"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="assistancewithbillorusage-questionsonspendinglimits"
	ownershipId="ASMS_Billing"
/>

# Pricing-I have questions about my spending limits

## **Recommended Steps**

### **How to Re-enable the subscription?**<br>
Your subscription might be disabled if the monthly credits on your subscription is used up. It will be re-activated when the credits are set back in the next billing cycle. If your subscription is disabled, check if
  * You have spending limit enabled or if you have deployed any third-party services. If so, please go ahead and remove the spending limit or delete/remove the service. Once the spending limit is removed, clear browser cache, cookies or use in-private browser to login to Azure portal to verify the subscription status, **or**
  * Wait until the next billing cycle when new credits would be added and the subscription would be automatically enabled, **or**
  * If you have a [Free Trial](https://azure.microsoft.com/free/) or an [Azure for Students Starter](https://azure.microsoft.com/offers/ms-azr-0144p/) subscription, you can upgrade to [Pay-As-You-Go](https://azure.microsoft.com/offers/ms-azr-0003p/) in the Azure portal: [Upgrade subscription](https://docs.microsoft.com/azure/cost-management-billing/manage/upgrade-azure-subscription)
  * If you would like to delete your Azure resources, follow the steps here: [Azure Resource deletion](https://docs.microsoft.com/azure/azure-resource-manager/management/delete-resource-group?tabs=azure-powershell)

### **How to remove spending limit in Azure portal?**<br>

1. Sign in to the [Azure Portal](https://portal.azure.com/) as Account Admin. Search **Cost Management + Billing**<br>
2. In **My subscriptions**, select your subscription. In the subscription overview, click the orange banner to remove the spending limit. Choose if you want to remove it indefinitely or for current billing period only.
  * **Remove spending limit indefinitely** will remove the spending limit without turning it on automatically at the start of the next billing period
  * **Remove spending limit for the current billing period** will remove the spending limit so that it turns back on automatically at the start of the next billing period<br>
**Note**: We don’t support custom spending limits<br>
[Understand Azure spending limit](https://docs.microsoft.com/azure/cost-management-billing/manage/spending-limit)

### **Understand when I will be charged?**<br>
The anniversary day is the day of the month you purchased the subscription. The invoice is generated on the anniversary date and 10 days later the credit card is charged. Invoice customers need to pay using Wire transfer/check and the details for payment is available on your monthly invoice.<br>
For example, if you purchased the subscription on January 15th, the anniversary day will be the 15th of each month when the invoice is generated and 10 days later the card is charged.

### **How to create and manage budgets?**<br>
Refer to this [tutorial](https://docs.microsoft.com/azure/cost-management-billing/costs/tutorial-acm-create-budgets#costs-in-budget-evaluations) for step by step guidance

### **How to use Cost alerts to monitor usage and spending?**<br>
Refer [use cost alerts](https://docs.microsoft.com/azure/cost-management-billing/costs/cost-mgt-alerts-monitor-usage-spending) to understand and use Cost Management alerts to monitor your Azure usage and spending and [prevent and analyze unexpected charges](https://docs.microsoft.com/azure/cost-management-billing/manage/getting-started) to help prevent them

### **Azure Free Account Services**<br>
For [Azure Free Account](https://azure.microsoft.com/offers/ms-azr-0044p/), we offer eligible customers $200 in Azure credits (Credits) to be used within the first 30 days of sign-up and 12 months of select [free services](https://azure.microsoft.com/free/) (services subject to change). Once all the benefits has been consumed for the free service, the usage is going to discount from the subscription credit. To prevent this, the resources needs to be deleted<br>

Learn more: [Resource deletion](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-delete)<br>
Learn more: [Azure Free Account FAQ](https://azure.microsoft.com/free/free-account-faq/)<br>

## **Recommended Documents**

* **Understand Billing model**
  * To understand your Azure bill refer: [Understand your bill](https://docs.microsoft.com/azure/cost-management-billing/understand/review-individual-bill)
  * Learn how to monitor usage and estimated Costs here: [Monitor usage and estimated costs](https://docs.microsoft.com/azure/azure-monitor/platform/usage-estimated-costs)
  * Learn about Azure service pricing and purchase options: [Azure Pricing](https://azure.microsoft.com/pricing/)
  * Configure and estimate the costs for Azure Products: [Pricing calculator](https://azure.microsoft.com/pricing/calculator/)
  * Learn more about service or specific pricing model: [Azure Purchase FAQ](https://azure.microsoft.com/pricing/faq/)
  * Speak with someone from sales about pricing: [Contact Azure Sales](https://azure.microsoft.com/overview/sales-number/)
  * Azure Subscriptions: [Microsoft Azure Offer Details](https://azure.microsoft.com/support/legal/offer-details/)
  * [Full list of Azure offers and the availability of the spending limit](https://azure.microsoft.com/support/legal/offer-details/)
* [Azure billing for external service charges](https://docs.microsoft.com/azure/cost-management-billing/understand/understand-azure-marketplace-charges)
* [Prevent unexpected charges with Azure billing and cost management](https://docs.microsoft.com/azure/cost-management-billing/manage/getting-started)
* [How to manage payment - Update, Change or Remove payment methods](https://docs.microsoft.com/azure/cost-management-billing/manage/change-credit-card)
* Check the list of supported countries/regions and currencies in the Purchase FAQ - [Supported countries/regions and currencies](https://azure.microsoft.com/pricing/faq/)
