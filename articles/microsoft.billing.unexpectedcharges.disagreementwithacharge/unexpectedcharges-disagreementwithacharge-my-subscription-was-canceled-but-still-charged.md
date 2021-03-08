<properties
 pageTitle="Canceled subscription and still see a charge"
	description="Canceled subscription and still see a charge"
	service="Microsoft.Billing"
	resource=""
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32783428"
	resourceTags=""
	productPesIds="17325"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="408bed60-b948-4e04-8178-696f6badaeae"
	ownershipId="ASMS_Billing"
/>
# Canceled subscription and still see a charge

## **Recommended Steps**

### **Canceled subscription and still see a charge**

These are the two most common scenarios why you're seeing a charge after canceling your subscription:

### **Scenario 1**

If you canceled your subscription during a billing period, you will receive an invoice after cancellation. This invoice is for the charges accumulated from the start of the billing period to the day the subscription was canceled.
  > For example, if a subscription with a billing period from the 5th of the month to the 4th of the next month is canceled on the 17th of the month, an invoice will be generated for the charges from 5th to 17th of the month. Charges will not stop the day the subscription was canceled.

**Compare billed charges with your usage file**

To find your invoices, follow these instructions:

1. In the Azure portal, enter `subscriptions` in the **search** box and then select **Subscriptions**
2. From the list of subscriptions, select your subscription
3. Under **Billing**, select **Invoices**
4. In the list of invoices, you can see each Billing period and when those charges were accrued. Look for the one that you want to download and select its download symbol. You might need to change the timespan to view older invoices. It might take a few minutes to generate the usage details file and invoice.
5. In the **Download Usage + Charges** window, select **Download invoice**.
6. To download a detailed breakdown of your Azure usage, select **Prepare usage file for download**.
7. Next, review the charges. Your invoice shows values for taxes and your usage charges.

For more details on how to compare usage and costs by downloading your invoice and usage files, see [Compare billed charges with your usage file](https://docs.microsoft.com/azure/cost-management-billing/understand/review-individual-bill#compare-billed-charges-with-your-usage-file).

### **Scenario 2**

You may have an active support plan associated with your subscription. Canceling the subscription does not automatically cancel the support plan. To prevent further charges and cancel a support plan, follow these steps:

**Cancel a support plan for MCA**

If you purchased your support plan through the Azure website, Azure portal, or if you have one under a Microsoft Customer Agreement, you can cancel a support plan. <br>If you purchased your support plan through a Microsoft representative or partner, contact them for assistance.

1. In the Azure portal, navigate to **Cost Management + Billing**
2. Under **Billing**, select **Recurring charges**
3. On the right-hand side for the support plan line item, select the ellipsis (...) and select **Turn off auto-renewal**

**Cancel a support plan for MOSP**

1. In the Azure portal, navigate to **Cost Management + Billing**
2. Navigate to **Subscriptions** and select the subscription
3. Select **Cancel** at the top

### **What happens after your cancel?**

After you cancel, your services are disabled. That means your virtual machines are de-allocated, temporary IP addresses are freed, and storage is read-only.

After your subscription is canceled, Microsoft waits 30 - 90 days before permanently deleting your data in case you need to access it, or you change your mind. We don't charge you for keeping the data. To learn more, see [Microsoft Trust Center - How we manage your data](https://go.microsoft.com/fwLink/p/?LinkID=822930&clcid=0x409).

## **Recommended Documents**

* [Review your individual Azure subscription bill](https://docs.microsoft.com/azure/cost-management-billing/understand/review-individual-bill)
* [Compare billed charges with your usage file](https://docs.microsoft.com/azure/cost-management-billing/understand/review-individual-bill#compare-billed-charges-with-your-usage-file)
* [What happens after subscription cancellation](https://docs.microsoft.com/azure/cost-management-billing/manage/cancel-azure-subscription#what-happens-after-subscription-cancellation)
* [Avoid charges with your Azure free account](https://docs.microsoft.com/azure/cost-management-billing/manage/avoid-charges-free-account)
