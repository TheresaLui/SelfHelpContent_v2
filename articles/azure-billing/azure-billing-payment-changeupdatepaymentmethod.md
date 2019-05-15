<properties
	pageTitle="change update payment method"
	description="change update payment method"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32632934"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="public"
	articleId="payment-changeupdatepaymentmethod"
/>

# change update payment method

## **Recommended Steps**

In the Account Center, as an Account Administrator, you can add a new credit card, update an existing credit card, or delete a credit card that you don't use.<br>

### **Add New/Use different Credit or Debit card**

1. Sign in to the [Account Center](https://account.windowsazure.com/Subscriptions) as the [Account Admin](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#whoisaa). Search on **Cost Management + Billing**
2. Select a Subscription you'd like to add the credit or debit card to. Select **Payment methods**
3. In the top-left corner, select “+” to add a card. A credit card form will appear on the right. Enter credit or debit card details
4. To make this card your active payment method, check the box next to Make this my active payment method above the form. This card will become the active payment instrument for all subscriptions using the same card as the selected subscription. Select **Next**
5. To **use a different credit card**, check the box next to the card you'd like to make the active payment method. Click **Set active**

### **Update/Change/Remove an existing Credit or Debit card**

1. Sign in to the [Account Center](https://account.windowsazure.com/Subscriptions) as the [Account Admin](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#whoisaa). Search on **Cost Management + Billing**
2. Select **Payment methods**. Click on the credit or debit card that you'd like to edit. A credit card form will appear on the right
3. Update the credit or debit card details. Select **Save**
4. To **remove**, check the box next to the card that you want to remove. _Note_: You can't remove your credit card if it is associated with other active Microsoft subscriptions. You will need to remove the credit card from all active subscriptions that you have with Microsoft and try again. Click **Delete**

### **Troubleshoot Error Scenarios**

1. **Unable to remove credit card from saved billing payment method**<br>
By design you cannot remove the card from the Active subscription. For an old/existing payment instrument to be deleted successfully,  a new card needs to be added to the subscription or you have to [Cancel the subscription](https://docs.microsoft.com/azure/billing/billing-how-to-cancel-azure-subscription). This will delete the subscription permanently and will also remove the card.<br>
**Note**: After a subscription has been disabled or canceled, there is a wait time of **90 days** before the subscription is permanently deleted. The payment method is kept on file during the retention period in case the subscription needs to be reactivated. After that period, the subscription is permanently deleted.
If the credit or debit card needs to be removed before the 90-day retention period ends, [Reactivate your subscription](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable)

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
Please log out of all the active azure sessions. Follow the below steps [here](http://www.thewindowsclub.com/launch-start-private-browsing) for in- Private session of the internet explorer, if using google chrome please use the incognito mode of the browsing. Once on in-private session, please follow the steps [here](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card) to update or change the credit card information.You could also try to Refresh browser, use another browser, delete cache cookies if above doesn't work

7. **Subscription still disabled after updating the payment method**<br>
It could be due to outstanding balance. Clear any outstanding balances before [re-activating the subscription](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable)

8. **Unable to change payment method due to an XML error response page**<br>
You might get this message if you are using [Ibiza portal](https://portal.azure.com/) to add new CC. You would need to login to the [Azure Account portal](https://account.azure.com/Subscriptions) using Account Admin’s email address to add card details.

If you want to update payment method to **'invoice'** (direct debit), please open a [support request](https://ms.portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview) so we can run a credit check before approving your request.<br>

Refer [Switch to Pay by Invoice](https://docs.microsoft.com/azure/billing/billing-how-to-pay-by-invoice) to change to invoice mode of payment<br>

**Note**:  Once moved to invoice mode of payment you cannot switch to credit card mode of payment and you cannot purchase any Azure market place services using  invoice mode of payment.

## **Recommended Documents**

* [Update, change, or remove payment methods](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card)
* [Set up invoicing](https://azure.microsoft.com/pricing/invoicing/)
