<properties
	pageTitle="issues with billing and payment"
	description="issues with billing and payment"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32632936"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="public"
	articleId="payment-issueswithbillingandpayment"
/>

# issues with billing and payment

### **Move resources to new resource group or subscription**

* Moving a resource only moves it to a new resource group. The move operation can't change the location of the resource. The new resource group may have a different location, but that doesn't change the location of the resource
* Learn more: [Tutorial: Move Azure resources to another resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-tutorial-move-resources)
* Learn more: [Services that can be moved](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources#services-that-can-be-moved)
* Learn more: [Checklist before moving resources](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources#checklist-before-moving-resources)

### **Stop email notifications from Azure**

1. Select your subscription from the [Subscriptions page](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade)<br>
2. Click **opt out of emailed invoices**. This option removes any email addresses set to receive invoices in email. If you opt back in, you will have to reconfigure recipients

### **Billing Alerts**

* If you’re the [Account Admin](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#whoisaa) for an Azure subscription, you can use the [Azure Billing Alert Service](https://docs.microsoft.com/azure/billing/billing-set-up-alerts) to create customized billing alerts that help you monitor and manage billing activity for your Azure accounts
* You can also download your invoice, or have it sent in email. However, only certain roles have permission to get billing invoice and usage information, like the Account Administrator<br>

Learn more: [Manage access to Azure billing using roles](https://docs.microsoft.com/azure/billing/billing-manage-access)<br>

Learn more: [How to download or view your Azure billing invoice and daily usage data](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date#noinvoice)<br>

### **Make Payments**

For Invoice (direct debit) payments, please send your payment to the location listed at the bottom of your invoice. If your payment isn't received or if we can't process your payment, you might get an email or see a Past due balance notification alert in the Account Center or Azure portal: [How to resolve past due balance for your Azure Subscription](https://docs.microsoft.com/azure/billing/billing-azure-subscription-past-due-balance)<br>

The payment may have failed to process if the credit card on file has expired or the charge was declined by your bank. The [Account Admin](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#whoisaa) can review and update the credit card in the Account Center: [How to add, update or remove a credit or debit card for Azure](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card) <br>

You might have your Azure subscription disabled because your credit is expired, you reached your spending limit, have an overdue bill, hit your credit card limit, or because the subscription was canceled by the Account Administrator. Follow the steps in the article below to get your subscription reactivated: [Why is my Azure subscription disabled and how do I reactivate it?](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable) <br>

### **Unexpected charges**

Learn more about how you can prevent unexpected charges with Azure billing and cost management [here](https://docs.microsoft.com/azure/billing/billing-getting-started). <br>


## **Recommended Documents**

* [Update, change, or remove payment methods](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card)
* [Set up invoicing](https://azure.microsoft.com/pricing/invoicing/)
* [Troubleshoot no subscriptions found issue in Azure portal or Account Center](https://docs.microsoft.com/azure/billing/billing-no-subscriptions-found)
* [Azure portal or Account Center sign-up issues](https://support.microsoft.com/help/4467267/can-t-sign-up-for-azure-in-azure-portal-or-azure-account-center)
* [Troubleshoot Sign-in Issues for Azure Subscription](https://support.microsoft.com/help/4042961/troubleshoot-why-you-can-t-sign-in-to-manage-your-azure-subscription)
* [Request/Download/View your Azure billing invoice and usage data](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date)
