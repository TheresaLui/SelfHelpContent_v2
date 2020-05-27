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
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="payment-changeupdatepaymentmethod"
	ownershipId="ASMS_Billing"
/>

# change update payment method

## **Recommended Steps**

In the Azure portal, as an Account Administrator, you can add a new credit card, update an existing credit card, or delete a credit card that you don't use. For [Microsoft Customer Agreement](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card#check-access-to-a-microsoft-customer-agreement),  payment methods are associated with [billing profiles](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card#change-payment-method-for-a-billing-profile). Only the user who signed up for Azure can update the payment method.

### **Troubleshoot Payment issues**
Refer [Troubleshoot payment issues/error scenarios](https://support.microsoft.com/help/4505172/troubleshooting-payment-issues) to see if it resolves your issue.

If there is a pending payment on the card since the card was denied by your financial institution, please reach out to your **financial institution** to resolve the issue. Use the below pointers:

   * You might have to check with the bank to see if the international transaction is enabled on the card
   * If card has credit limit to settle the balance
   * If recurring payment is enabled on the card

### **Add a new Credit or Debit card to an Azure Subscription**

1. Sign in to the [Azure portal](https://portal.azure.com/) as the [Account Admin](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#whoisaa). Search on **Cost Management + Billing**
2. Select a Subscription you'd like to add the credit or debit card to. Select **Payment methods**
3. In the top-left corner, select + to add a card. A credit card form will appear on the right. Enter credit or debit card details
4. To make this card your active payment method, check the box next to Make this my active payment method above the form. This card will become the active payment instrument for all subscriptions using the same card as the selected subscription. Select **Next**
5. To **use a different credit card**, check the box next to the card you'd like to make the active payment method. Click **Set active**

### **Update/Change/Remove an existing Credit or Debit card**

1. Sign in to the [Azure portal](https://portal.azure.com/) as the [Account Admin](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#whoisaa). Search on **Cost Management + Billing**.
2. Select **Payment methods**. Click on the credit or debit card that you'd like to edit. A credit card form will appear on the right
3. Update the credit or debit card details. Select **Save**.
4. To **remove**, check the box next to the card that you want to remove

_Note_: You can't remove your credit card if it is associated with other active Microsoft subscriptions. You will need to remove the credit card from all active subscriptions that you have with Microsoft and try again. Click **Delete**

Learn more: [Update, change, or remove payment methods](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card)

### **Switch to Pay by Invoice**

* If you want to update payment method to **'invoice'** (direct debit), please open a [support request](https://ms.portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview) so we can run a credit check before approving your request
* Refer [Switch to Pay by Invoice](https://docs.microsoft.com/azure/billing/billing-how-to-pay-by-invoice) to change to invoice mode of payment<br>

**Note**: Once moved to invoice mode of payment you cannot switch to credit card mode of payment and you cannot purchase any Azure marketplace services using invoice mode of payment.

## **Recommended Documents**

* [Set up invoicing](https://azure.microsoft.com/pricing/invoicing/)
* [Change payment method- FAQ](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card#frequently-asked-questions)
* [Change payment method for a billing profile](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card#change-payment-method-for-a-billing-profile)
* [Check access to a Microsoft Customer Agreement](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card#check-access-to-a-microsoft-customer-agreement)
