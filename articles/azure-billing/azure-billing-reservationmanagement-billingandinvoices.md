<properties
	pageTitle="Reservation billing and invoice"
	description="Reservation billing and invoice"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32593229"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="public,BlackForest, Fairfax, MoonCake, usnat, ussec"
	articleId="d6753434-706e-45f3-a11d-fbbfe7107dd2"
	ownershipId="ASMS_Billing"
/>

# Reservation billing and invoice

### **Billing for Reserved Instance purchase**

The reserved instance purchase is charged to the payment method tied to the subscription that you select at the time of purchase. The subscription type must be an enterprise agreement (offer number: MS-AZR-0017P), Pay-As-You-Go (offer number: MS-AZR-0003P), Microsoft Customer Agreement or CSP.

* For an enterprise subscription, the charges are deducted from the enrollment's monetary commitment balance or charged as overage
* For Pay-As-You-Go subscription, the charges are billed to the credit card or invoice payment method on the subscription
 
### **Download your invoice from Azure portal (.pdf)**

* Select your subscription from the [Subscriptions](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade) page in Azure portal as [a user with access to invoices](https://docs.microsoft.com/azure/billing/billing-manage-access)
* Select **Invoices**
* Click **Download Invoice** to view a copy of your PDF invoice. If it says **Not available**, see [Why don't I see an invoice for the last billing period?](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date#noinvoice)

### **Receive your invoice in email (.pdf)**

* Select your subscription from the [Subscriptions](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade) page. Click **Invoices** then Email my invoice
* Click **opt in** and accept the terms. You will have to opt in for each subscription you own

Note: If you don't get an email after following the steps, make sure your email address is correct in the [communication preferences on your profile](https://account.windowsazure.com/profile)
	
### **Download your usage data from the Azure portal**

* Sign into the [Azure Account Center](https://account.windowsazure.com/Subscriptions) as the [Account Admin](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#whoisaa)
* Select the subscription for which you want the invoice and usage information
* Select **Billing History**
* Select **View Current Statement** to see an estimate of your charges at the time the estimate was generated
* Select **Download Usage** to download the daily usage data as a CSV file. If you see two versions available, download version 2

Other questions: [Visit reserved instance docs](https://docs.microsoft.com/azure/billing/billing-save-compute-costs-reservations)

### **Unable to see invoice for the last billing period**
Some possible reasons you might not see an invoice:

* You have a monthly credit amount with your subscription that you didn't exceed or you have a Free Trial. An invoice is only generated when you owe money
* It's less than 30 days from the day you subscribed to Azure
* The invoice isn't generated yet. Wait until the end of the billing period
* If you're not the Account Administrator, older invoices may not be available to you

## **Recommended Documents**

* [Billing basics](https://docs.microsoft.com/partner-center/billing-basics/)
* [Understand how the Reserved Instance discount is applied](https://docs.microsoft.com/azure/billing/billing-understand-vm-reservation-charges/)
* [Download or view your Azure billing invoice and daily usage data](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date)
* [Understand how the Reserved Instance discount is applied](https://docs.microsoft.com/azure/billing/billing-understand-vm-reservation-charges/)
* [Understand Reserved Instance usage for your Pay-As-You-Go subscription](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage/)
* [Understand Reserved Instance usage for your Enterprise enrollment](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage-ea/)
* [Windows software costs not included with Reserved instances](https://docs.microsoft.com/azure/billing/billing-reserved-instance-windows-software-costs/)
* [Reserved Instances in Partner Central Cloud Solution Provider (CSP) program](https://docs.microsoft.com/partner-center/azure-reservations/)
