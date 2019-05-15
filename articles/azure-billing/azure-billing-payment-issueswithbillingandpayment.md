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

# my issue is not listed here

### **Request Azure invoice**

* [Invoice over email](https://azure.microsoft.com/blog/azure-email-invoices/)
* [Download from Azure Account Centre](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date)
* [Allowing additional users to access invoices](https://docs.microsoft.com/azure/billing/billing-manage-access)

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

### **Troubleshoot payment error scenarios**

1. **Unable to remove credit card from saved billing payment method**<br>
By design you cannot remove the card from the Active subscription. For an old/existing payment instrument to be deleted successfully,  a new card needs to be added to the subscription or you have to [Cancel the subscription](https://docs.microsoft.com/azure/billing/billing-how-to-cancel-azure-subscription). This will delete the subscription permanently and will also remove the card.<br>
**Note**: After a subscription has been disabled or canceled, there is a wait time of **90 days** before the subscription is permanently deleted. The payment method is kept on file during the retention period in case the subscription needs to be reactivated. After that period, the subscription is permanently deleted.
If the credit or debit card needs to be removed before the 90-day retention period ends, [Reactivate your subscription](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable)

2. **Unable to delete old payment method after adding new payment method**<br>
The new payment instrument might not be associated with the subscription. To help associate the payment instrument to the subscription refer [here](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card). Additionally, to troubleshoot issues with declined card refer [Troubleshoot a declined card issue](https://support.microsoft.com/help/4488948/troubleshoot-declined-card-at-azure-sign-up)

3. **Unable to delete payment method due to error message "Cannot delete payment method"**<br>
It could be due to an outstanding balance. Clear any outstanding balances before deleting the payment method.

4. **Unable to see subscriptions under my account to update the payment method**<br>
You might be using a different email id and the subscriptions might be aligned to another email id. Refer [No subscriptions found in Azure portal](https://docs.microsoft.com/azure/billing/billing-no-subscriptions-found) to troubleshoot this issue

5. **Unable to make payment for a subscription due to error message "Payment is past due. There is a problem with your payment method" or "We're sorry, the information cannot be saved. Close the browser and try again"**<br>
This could be because there is a pending payment on the card since the card was denied by your financial institution. Please make sure that the credit card has sufficient balance to make payment or use some other card for making payment or reach out to your financial institution to resolve the issue. Use the below pointers

1. You might have to check with the bank to see if the international transaction is enabled on the card<br>
2. If card has credit limit to settle the balance<br>
3. If recurring payment is enabled on the card<br>
	
6. **Unable to change payment method due to browser issues (Browser hangs, keeps spinning, does not load, etc.)**<br>
Please log out of all the active azure sessions. Follow the below steps [here](http://www.thewindowsclub.com/launch-start-private-browsing) for in- Private session of the internet explorer, if using google chrome please use the incognito mode of the browsing. Once on in-private session, please follow the steps [here](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card) to update or change the credit card information.You could also try to Refresh browser, use another browser, delete cache cookies if above doesn't work

7. **Subscription still disabled after updating the payment method**<br>
It could be due to outstanding balance. Clear any outstanding balances before [re-activating the subscription](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable)

8. **Unable to change payment method due to an XML error response page**<br>
You might get this message if you are using [Ibiza portal](https://portal.azure.com/) to add new CC. You would need to login to the [Azure Account portal](https://account.azure.com/Subscriptions) using Account Admin’s email address to add card details.


### **Unexpected charges**

Learn more about how you can prevent unexpected charges with Azure billing and cost management [here](https://docs.microsoft.com/azure/billing/billing-getting-started). <br>


## **Recommended Documents**

* [Update, change, or remove payment methods](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card)
* [Set up invoicing](https://azure.microsoft.com/pricing/invoicing/)
* [Troubleshoot no subscriptions found issue in Azure portal or Account Center](https://docs.microsoft.com/azure/billing/billing-no-subscriptions-found)
* [Azure portal or Account Center sign-up issues](https://support.microsoft.com/help/4467267/can-t-sign-up-for-azure-in-azure-portal-or-azure-account-center)
* [Troubleshoot Sign-in Issues for Azure Subscription](https://support.microsoft.com/help/4042961/troubleshoot-why-you-can-t-sign-in-to-manage-your-azure-subscription)
* [Request/Download/View your Azure billing invoice and usage data](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date)
* [Transfer ownership of an Azure subscription to another account](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)
* [Pay Azure subscription by invoice](https://docs.microsoft.com/azure/billing/billing-how-to-pay-by-invoice)
