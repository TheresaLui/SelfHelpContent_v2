<properties
	pageTitle="request invoices"
	description="request invoices"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32593229"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="public"
	articleId="d6753434-706e-45f3-a11d-fbbfe7107dd2"
/>

# Request Invoices

## Recommended Steps

### How is a reserved instance purchase billed?

The reserved instance purchase is charged to the payment method tied to the subscription. The payment method on the subscription is charged the upfront costs for the Reserved Instance. The subscription type must be an enterprise agreement (offer number: MS-AZR-0017P) or Pay-As-You-Go (offer number: MS-AZR-0003P). For an enterprise subscription, the charges are deducted from the enrollment's monetary commitment balance or charged as overage. For Pay-As-You-Go subscription, the charges are billed to the credit card or invoice payment method on the subscription.<br>
To Learn more, see [Understanding billing for Reserved instances](https://docs.microsoft.com/azure/billing/billing-understand-vm-reservation-charges)<br>

### To download your invoice from Azure portal (.pdf)

* Select your subscription from the [Subscriptions](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade) page in Azure portal as [a user with access to invoices](https://docs.microsoft.com/azure/billing/billing-manage-access).<br>
* Select **Invoices**.<br>
* Click **Download Invoice** to view a copy of your PDF invoice. If it says **Not available**, see [Why don't I see an invoice for the last billing period?](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date#noinvoice)<br>

### To get your invoice in email (.pdf)

* Select your subscription from the [Subscriptions](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade) page.  Click **Invoices** then Email my invoice.<br>
* Click **opt in** and accept the terms. You will have to opt in for each subscription you own<br>
_Note:_ If you don't get an email after following the steps, make sure your email address is correct in the [communication preferences on your profile](https://account.windowsazure.com/profile).<br>

### To download your usage from the Account Center(.csv)

* Sign into the [Azure Account Center](https://account.windowsazure.com/Subscriptions) as the [Account Admin](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#whoisaa)<br>
* Select the subscription for which you want the invoice and usage information<br>
* Select **Billing History**<br>
* Select **View Current Statement** to see an estimate of your charges at the time the estimate was generated.<br>
* Select **Download Usage** to download the daily usage data as a CSV file. If you see two versions available, download version 2.<br>

Instead of [downloading your invoice](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date) every month, you can now opt-in to receive your invoice statement attached to your monthly billing email: [Azure invoices emailed direct to your inbox](https://azure.microsoft.com/blog/azure-email-invoices/) <br>

### Unable to see invoice for the last billing period
Some possible reasons you might not see an invoice :
   * You have a monthly credit amount with your subscription that you didn't exceed or you have a Free Trial. An invoice is only generated when you owe money.<br>
   * It's less than 30 days from the day you subscribed to Azure.<br>
   * The invoice isn't generated yet. Wait until the end of the billing period.<br>
   * If you're not the Account Administrator, older invoices may not be available to you.<br>

## **Recommended Documents**

* [Manage Azure Reserved VM Instances billing](https://docs.microsoft.com/partner-center/azure-reservations-billing/)
* [Billing basics](https://docs.microsoft.com/partner-center/billing-basics/)
* [Understand how the Reserved Instance discount is applied](https://docs.microsoft.com/azure/billing/billing-understand-vm-reservation-charges/)
* [Download or view your Azure billing invoice and daily usage data](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date)
* [Understand how the Reserved Instance discount is applied](https://docs.microsoft.com/azure/billing/billing-understand-vm-reservation-charges/)
* [Understand Reserved Instance usage for your Pay-As-You-Go subscription](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage/)
* [Understand Reserved Instance usage for your Enterprise enrollment](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage-ea/)
* [Windows software costs not included with Reserved instances](https://docs.microsoft.com/azure/billing/billing-reserved-instance-windows-software-costs/)
* [Reserved Instances in Partner Central Cloud Solution Provider (CSP) program](https://docs.microsoft.com/partner-center/azure-reservations/)


