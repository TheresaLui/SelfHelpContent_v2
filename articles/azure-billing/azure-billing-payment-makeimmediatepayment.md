<properties
	pageTitle="make immediate payment"
	description="make immediate payment"
	service="azure-billing"
	resource="billing"
	authors="lishepar"
	ms.author="lishepar"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32632937"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="payment-makeimmediatepayment"
	ownershipId="ASMS_Billing"
/>

# Make immediate payment

If you want to make an immediate payment for your invoice, first you'll have to verify your account type.

### **Check the type of your account**

1. Navigate to **Cost Management + Billing**.
1. Select **Properties** from the left-hand side. The **Type** field on the properties page determines the type of your account. It can be:
    - Microsoft Online Service Program
    - Microsoft Customer Agreement
    - Enterprise Agreement
    - Microsoft Partner Agreement

For more information, see [View your billing accounts in Azure portal](https://docs.microsoft.com/azure/cost-management-billing/manage/view-all-accounts).

## **Recommended steps**

After you verify your account type, follow the steps below to make an immediate payment.

### **How to pay if you have Microsoft Online Service Program**

1. Navigate to **Cost Management + Billing**.
1. Select the past due subscription from the **Overview** page.
1. In the **Subscription overview** page, select the red past due banner to settle the balance.
    If you are not the Account Administrator, you will not be able to settle the balance.
1. In the new **Settle balance** page, select **Select payment method**.
1. In the new blade on the right, select a credit card from the drop-down or add a new one by selecting the blue **Add new payment method** link.

    This credit card will become the active payment method for all subscriptions currently using the failed payment method.
    The total outstanding balance reflects outstanding charges across all Microsoft services using the failed payment method. If the selected payment method also has outstanding charges for Microsoft services, this will be reflected in the total outstanding balance. You must pay those outstanding charges, too.
1. Select  **Pay**.

   For more information, see [Resolve past due balance in the Azure portal](https://docs.microsoft.com/azure/cost-management-billing/manage/resolve-past-due-balance#resolve-past-due-balance-in-the-azure-portal).

### **How to pay if you have Microsoft Customer Agreement**

To pay invoices in the Azure portal, you must have the correct [MCA permissions](https://docs.microsoft.com/azure/cost-management-billing/manage/understand-mca-roles). For more information, see [Pay now in the Azure portal](https://docs.microsoft.com/azure/cost-management-billing/understand/pay-bill#pay-now-in-the-azure-portal).

1. Search on **Cost Management + Billing**.
2. In the left menu, select **Invoices** under **Billing**.
3. If any of your invoices are due or past due, you'll see a blue **Pay now** link for that invoice. Select **Pay now**.
4. In the **Pay now** window, select **Select a payment method** to choose an existing credit card or add a new one.
5. After you select a payment method, select **Pay now**.

   The invoice status should show as **paid** within 24 hours.

   For more information, see [How to pay your bill for Microsoft Azure](https://docs.microsoft.com/azure/cost-management-billing/understand/pay-bill) for Microsoft Customer Agreement (MCA) accounts.

### **How to pay your invoice by credit or debit card**

If the default payment method for your billing profile is a credit or debit card, it's automatically charged each billing period.

If your automatic credit or debit card charge gets declined for any reason, you can make a one-time payment with a credit or debit card in the Azure portal using **Pay now**.

If you want to learn how to change your default payment method to check or wire transfer, see [How to pay by invoice](https://docs.microsoft.com/azure/cost-management-billing/manage/pay-by-invoice).

### **How to pay your invoice by check or wire transfer**

If the default payment method of your billing profile is check or wire transfer, follow the payment instructions shown on your invoice PDF file.

Alternatively, if your invoice is under the threshold amount for your currency, you can make a one-time payment in the Azure portal with a credit or debit card using **Pay now**. If your invoice amount exceeds the threshold, you can't pay your invoice with a credit or debit card. You'll find the threshold amount for your currency in the Azure portal after selecting **Pay now**.

For more information, see [Pay by default payment method](https://docs.microsoft.com/azure/cost-management-billing/understand/pay-bill#pay-by-default-payment-method).

### **Troubleshooting payments with credit or debit card**

- In order to be able to make an immediate payment, make sure to [resolve past due balances](https://docs.microsoft.com/azure/billing/billing-azure-subscription-past-due-balance?WT.mc_id=Portal-Microsoft_Azure_Support) and [pay your bill](https://docs.microsoft.com/azure/cost-management-billing/understand/pay-bill). If your payment isn't received or if Azure can't process your payment, you might get an email or see a Past due balance notification alert in the Azure portal.
- The payment may have failed to process if the credit card on file has expired or the charge was declined by your bank. If you're an [Account Admin](https://docs.microsoft.com/azure/billing/billing-subscription-transfer?WT.mc_id=Portal-Microsoft_Azure_Support) or if you have the correct [MCA permissions](https://docs.microsoft.com/azure/cost-management-billing/manage/understand-mca-roles), you can review and update the credit card in the Azure portal as documented at [Add/Update my payment method](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card?WT.mc_id=Portal-Microsoft_Azure_Support).
- You might have your Azure subscription disabled because:
    - Your credit is expired
    - You've reached your spending limit
    - Have an overdue bill
    - Hit your credit card limit
    - The subscription was canceled by the Account Administrator or someone with the correct [MCA permissions](https://docs.microsoft.com/azure/cost-management-billing/manage/understand-mca-roles).

    Follow the steps in the article below to get your subscription reactivated: [Reactivate my subscription](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable?WT.mc_id=Portal-Microsoft_Azure_Support).

- If there's a pending payment on the card since the card was denied by your financial institution, contact your **financial institution** to resolve the issue and keep in mind:
  - You might have to check with the bank to see if the international transaction is enabled on the card.
  - If card has credit limit to settle the balance.
  - If recurring payment is enabled on the card.

Check the [Payment FAQ](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card?WT.mc_id=Portal-Microsoft_Azure_Support) to see if it resolves your issue.

### **How to pay if you have a Enterprise Agreement or Microsoft Partner Agreement**

For more information on Enterprise Agreements see [Understand your Azure Enterprise Agreement bill](https://docs.microsoft.com/azure/cost-management-billing/understand/review-enterprise-agreement-bill).

For more information on Microsoft Partner Agreement see [Review your Microsoft Partner Agreement invoice](https://docs.microsoft.com/azure/cost-management-billing/understand/review-partner-agreement-bill).

## **Recommended Documents**

- [How to pay your bill](https://docs.microsoft.com/azure/cost-management-billing/understand/pay-bill)
- [How to resolve your past due balance for your Azure subscription](https://docs.microsoft.com/azure/cost-management-billing/manage/resolve-past-due-balance)
- [Add or update a payment method](https://docs.microsoft.com/azure/cost-management-billing/manage/change-credit-card?WT.mc\_id=Portal-Microsoft\_Azure\_Support)
- [Deleting a credit or debit card](https://docs.microsoft.com/azure/cost-management-billing/manage/delete-azure-payment-method)
- [Get approved for invoice pay](https://docs.microsoft.com/azure/cost-management-billing/manage/pay-by-invoice)
- [Manage access to billing information in Azure](https://docs.microsoft.com/azure/cost-management-billing/manage/manage-billing-access?WT.mc\_id=Portal-Microsoft\_Azure\_Support)
- [View and download your Azure invoice](https://docs.microsoft.com/azure/cost-management-billing/understand/download-azure-invoice)
- [Allowing additional users to access invoices](https://docs.microsoft.com/azure/billing/billing-manage-access?WT.mc_id=Portal-Microsoft_Azure_Support)
- [Learn more about Billing accounts and scopes in the Azure portal](https://docs.microsoft.com/azure/cost-management-billing/manage/view-all-accounts)
