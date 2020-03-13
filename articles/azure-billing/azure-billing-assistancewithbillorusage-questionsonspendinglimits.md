<properties
	pageTitle="I have questions about my spending limits"
	description="I have questions about my spending limits"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32632938"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake"
	articleId="assistancewithbillorusage-questionsonspendinglimits"
	ownershipId="ASMS_Billing"
/>

# I have questions about my spending limits

## **Recommended Steps**

### **Re-enable the subscription**

Your subscription might be disabled if the monthly credits on your subscription is used up. It will be re-activated when the credits are set back in the next billing cycle. If your subscription is disabled, check if

* You have spending limit enabled or if you have deployed any third-party services. If so, please go ahead and remove the spending limit or delete/remove the service. Once the spending limit is removed, clear browser cache, cookies or use in-private browser to login to Azure portal to verify the subscription status, **or**
* Wait until the next billing cycle when new credits would be added and the subscription would be automatically enabled, **or**	
* If you have a [Free Trial](https://azure.microsoft.com/free/) or an [Azure for Students Starter](https://azure.microsoft.com/offers/ms-azr-0144p/) subscription, you can upgrade to [Pay-As-You-Go](https://azure.microsoft.com/offers/ms-azr-0003p/) in the Azure portal: [Upgrade subscription](https://docs.microsoft.com/azure/billing/billing-upgrade-azure-subscription)
* If you would like to delete your Azure resources, follow the steps here: [Azure Resource deletion](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-delete)


### **Remove spending limit in Account Center**

1. Sign in to the [Account Center](https://account.windowsazure.com/Subscriptions). Select a subscription. If the subscription is disabled due to the spending limit being reached, click this notification: "_Subscription reached the Spending Limit and has been disabled to prevent charges._" Otherwise, click **Remove spending limit** in the **Subscription Status** area.
2. Select an option that is appropriate for you:

   * **Remove spending limit indefinitely** will remove the spending limit without turning it on automatically at the start of the next billing period
   * **Remove spending limit for the current billing period** will remove the spending limit so that it turns back on automatically at the start of the next billing period<br>
   
_Note:_ We don’t support custom spending limits.	
  * Learn more: [Azure Spending Limit and how to remove it](https://docs.microsoft.com/azure/billing/billing-spending-limit) <br>
  * Learn more: [Set Billing alerts](https://blogs.technet.microsoft.com/uspartner_ts2team/2015/05/31/how-to-set-up-billing-alerts-in-azure-using-the-billing-alert-service-preview/)
  * Learn more: [Set budget and cost alerts](https://docs.microsoft.com/azure/billing/billing-getting-started#use-budgets-and-cost-alerts)

### **View/Add Credits**

**View/Add Credits to your Azure In Open subscription**

* Go to [Azure in Open](https://azure.microsoft.com/offers/ms-azr-0111p/). Click **Add Credits** under Existing subscription option and follow the steps

**Check Sponsorship credits**

* Go to [Azure Sponsorship Offer](https://www.microsoftazuresponsorships.com/). Click **Check your Balance**
Note: Only Account Admin of Sponsorship can check the credits

**Check Usage/Invoice**

* Sign in to the [Account Center](https://account.windowsazure.com/Subscriptions) as the [Account Admin](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#whoisaa).Click on the subscription type -> Billing history, where you can download the Invoice and usage report
	
### **Azure Free Account Services**
For [Azure Free Account](https://azure.microsoft.com/offers/ms-azr-0044p/), we offer eligible customers $200 in Azure credits (Credits) to be used within the first 30 days of sign-up and 12 months of select [free services](https://azure.microsoft.com/free/) (services subject to change). Once all the benefits has been consumed for the free service, the usage is going to discount from the subscription credit. To prevent this, the resources needs to be deleted <br>

* Learn more: [Resource deletion](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-delete)<br>
* Learn more: [Azure Free Account FAQ](https://azure.microsoft.com/free/free-account-faq/)<br>

**Azure SSIS IR**: Learn more on how to stop-set-start the Azure SSIS IR [here](https://docs.microsoft.com/azure/data-factory/manage-azure-ssis-integration-runtime)<br>

### **Understand Billing model**

* To understand your Azure bill refer: [Understand your bill](https://docs.microsoft.com/azure/billing/billing-understand-your-bill)
* Learn how to monitor usage and estimated Costs here: [Monitor usage and estimated costs](https://docs.microsoft.com/azure/azure-monitor/platform/usage-estimated-costs)
* Learn about Azure service pricing and purchase options: [Azure Pricing](https://azure.microsoft.com/pricing/)
* Configure and estimate the costs for Azure Products: [Pricing calculator](https://azure.microsoft.com/pricing/calculator/ )
* Learn more about service or specific pricing model: [Azure Purchase FAQ](https://azure.microsoft.com/pricing/faq/)
* Speak with someone from sales about pricing: [Contact Azure Sales](https://azure.microsoft.com/overview/sales-number/)
* Azure Subscriptions: [Microsoft Azure Offer Details](https://azure.microsoft.com/support/legal/offer-details/)

## **Recommended Documents**

* [Full list of Azure offers and the availability of the spending limit](https://azure.microsoft.com/support/legal/offer-details/)
* [Azure billing for external service charges](https://docs.microsoft.com/azure/billing/billing-understand-your-azure-marketplace-charges)
* [Prevent unexpected charges with Azure billing and cost management](https://docs.microsoft.com/azure/billing/billing-getting-started)
* [How to manage payment - Update, Change or Remove payment methods](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card)
* Check the list of supported countries/regions and currencies in the Purchase FAQ - [Supported countries/regions and currencies](https://azure.microsoft.com/pricing/faq/)
