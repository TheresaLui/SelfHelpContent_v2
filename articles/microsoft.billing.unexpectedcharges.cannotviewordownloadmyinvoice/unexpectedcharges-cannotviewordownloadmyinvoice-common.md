<properties
	pageTitle="Cannot view or download invoices"
	description="Cannot view or download invoices"
	service="Microsoft.Billing"
	resource=""
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32783402,32783404,32783406,32783407,32783409,32783426,32783429,32783430,32783437,32783440"
	resourceTags=""
	productPesIds="17325"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="654fbf74-4fb2-4370-a0a1-e5e814467147"
	ownershipId="ASMS_Billing"
/>
# cannot view or download invoices

## **Recommended Steps**

### **Troubleshoot: Unable to see invoice for the last billing period?**

**Some possible reasons you might not see an invoice**

- You have a monthly credit amount with your subscription that you didn't exceed or you have a Free Trial. An invoice is only generated when you owe money.
- It's less than 30 days from the day you subscribed to Azure.
- The invoice isn't generated yet. Wait until the end of the billing period.
- If you're not the Account Administrator, older invoices may not be available to you.
**Note**: Microsoft doesn't provide any usage reports or consumption data to Azure CSP customers. Partner Center usage data is partner-facing.

Learn more on [AIO Azure in open](https://azure.microsoft.com/offers/ms-azr-0111p/).

### **How to find account type**

The instructions to download your invoice vary by the type of your billing account. To identify your billing account type:

1. Navigate to **Cost Management + Billing**
2. Select **Properties** from the left-hand side. The **Type** field on the properties page determines the type of your account. It can be:
  - Microsoft Online Service Program
  - Microsoft Customer Agreement
  - Microsoft Partner Agreement
  - Enterprise Agreement

For more detailed instruction on how to check the type of account see [Check the type of your account](https://docs.microsoft.com/azure/cost-management-billing/manage/view-all-accounts#check-the-type-of-your-account).

### **Microsoft Online Service Program (MOSP)**

**Download your Azure subscription invoice (.pdf)**

1. Select your subscription from the [Subscriptions page](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade) in Azure portal as [a user with access to invoices](https://docs.microsoft.com/azure/cost-management-billing/manage/manage-billing-access?WT.mc_id=Portal-Microsoft_Azure_Support) then select **Invoices**.
2. Click **Download Invoice** to view a copy of your PDF invoice. If it says **Not available**, see [Why don't I see an invoice for the last billing period?](https://docs.microsoft.com/azure/cost-management-billing/manage/download-azure-invoice-daily-usage-date?WT.mc_id=Portal-Microsoft_Azure_Support#noinvoice).
3. You can also view your daily usage by clicking the billing period To obtain a PDF of your invoice and a copy of your detailed daily usage file (.CSV): [Get invoice and usage data](https://docs.microsoft.com/azure/cost-management-billing/manage/download-azure-invoice-daily-usage-date?WT.mc_id=Portal-Microsoft_Azure_Support).

**Get your invoice in email (.pdf)**

1. Select your subscription from the [Subscriptions page](https://ms.portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade). Click **Invoices** then **Email my invoice**.
2. Click **opt in** and accept the terms. You will have to opt in for each subscription you own.
   >Note: If you don't get an email after following the steps, make sure your email address is correct in the [communication preferences on your profile](https://account.windowsazure.com/profile). [Azure invoices emailed direct to your inbox](https://azure.microsoft.com/blog/azure-email-invoices/).

**Download usage in Azure portal**

1. Select your subscription from the [Subscriptions page](https://ms.portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade) in the Azure portal as [a user with access to invoices](https://docs.microsoft.com/azure/cost-management-billing/manage/manage-billing-access?WT.mc_id=Portal-Microsoft_Azure_Support).
2. Select **Invoices**.
3. Click the download button of a invoice period that you want to check.
4. Download a daily breakdown of consumed quantities and estimated charges by clicking **Download csv**. This may take a few minutes to prepare the csv file.

**Download your Azure support plan invoice (.pdf)**

1. Select your subscription from the [Subscriptions page](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade) in the Azure portal.
2. Select **Invoices** from the billing section.
3. Select the invoice that you want to download and then click **Download invoices**.
4. You can also download a daily breakdown of consumed quantities and charges by clicking the download icon and then clicking **Prepare Azure usage file** button under the usage details section. It may take a few minutes to prepare the CSV file.

For more information about your invoice, see [Understand your bill for Microsoft Azure](https://docs.microsoft.com/en-us/azure/cost-management-billing/understand/review-individual-bill). For help identify unusual costs, see [Analyze unexpected charges](https://docs.microsoft.com/en-us/azure/cost-management-billing/understand/analyze-unexpected-charges).

### **Microsoft Customer Agreement (MCA)**

**Get your Microsoft Customer Agreement invoices in email**

If you have a Microsoft Customer Agreement, you can opt in to get your invoice in an email. All billing profile Owners, Contributors, Readers, and Invoice managers will get the invoice by email. Readers cannot update the email invoice preference.

1. Search for  **Cost Management + Billing**.
1. Select a **billing profile**. Under Settings, select **Properties**.
1. Under Email Invoice, select **Update email invoice preference**. Select opt in. Click **Update**.

**Download usage for your Microsoft Customer Agreement**

To view and download usage data for a billing profile, you must be a billing profile Owner, Contributor, Reader, or Invoice manager.

**Download usage for billed charges**

  - Search for **Cost Management + Billing**. Select a billing profile. Select **Invoices**.
  - In the invoice grid, find the row of the invoice corresponding to the usage you want to download.
  - Click on the ellipsis (...) at the end of the row. In the download context menu, select **Azure usage and charges**.

**Download usage for open charges**

  - Search for **Cost Management + Billing**. Select a billing profile.
  - In the Overview blade, click **Download Azure usage and charges** For Microsoft Customer Agreement, refer to: [Get invoice in email for a Microsoft Customer Agreement](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date?WT.mc_id=Portal-Microsoft_Azure_Support#get-your-invoice-in-email-pdf).

### **Enterprise Agreement (EA)**

To view and download usage data as a EA customer, you must be an Enterprise Administrator, Account Owner, or Department Admin with the view charges policy enabled.

  - Sign in to the Azure portal. Search for **Cost Management + Billing**.
  - Select **Usage + charges**. For the month you want to download, select **Download**.

## **Recommended Documents**

- [Why you might not see an invoice?](https://docs.microsoft.com/azure/cost-management-billing/understand/download-azure-invoice?WT.mc_id=Portal-Microsoft_Azure_Support#noinvoice)
- [Request/Download/View your Azure billing invoice and usage data](https://docs.microsoft.com/azure/cost-management-billing/manage/download-azure-invoice-daily-usage-date?WT.mc_id=Portal-Microsoft_Azure_Support)
- [How to email Azure invoices directly to your inbox](https://docs.microsoft.com/azure/cost-management-billing/manage/download-azure-invoice-daily-usage-date?WT.mc_id=Portal-Microsoft_Azure_Support)
- [Understand detailed usage charges](https://docs.microsoft.com/azure/cost-management-billing/understand/review-individual-bill?WT.mc_id=Portal-Microsoft_Azure_Support#csv)
- [Understand terms on your invoice](https://docs.microsoft.com/azure/cost-management-billing/understand/understand-invoice?WT.mc_id=Portal-Microsoft_Azure_Support)
- [Understand Azure CSP invoice](https://docs.microsoft.com/partner-center/azure-plan-lp?WT.mc_id=Portal-Microsoft_Azure_Support)
- [Understand terms on your detailed usage](https://docs.microsoft.com/azure/cost-management-billing/understand/understand-usage?WT.mc_id=Portal-Microsoft_Azure_Support)
- [How to Transfer ownership](https://docs.microsoft.com/azure/cost-management-billing/manage/billing-subscription-transfer?WT.mc_id=Portal-Microsoft_Azure_Support)
- [How to Reactivate subscription](https://docs.microsoft.com/azure/cost-management-billing/manage/subscription-disabled?WT.mc_id=Portal-Microsoft_Azure_Support)
- [How to Cancel subscription](https://docs.microsoft.com/azure/cost-management-billing/manage/cancel-azure-subscription?WT.mc_id=Portal-Microsoft_Azure_Support)
- [Azure subscription and service limits, quotas and constraints](https://docs.microsoft.com/azure/azure-resource-manager/management/azure-subscription-service-limits?WT.mc_id=Portal-Microsoft_Azure_Support)
- [Azure spending limit](https://docs.microsoft.com/azure/cost-management-billing/manage/spending-limit?WT.mc_id=Portal-Microsoft_Azure_Support)
- Learn more on Marketplace invoice and usage: [Azure marketplace charges](https://docs.microsoft.com/azure/cost-management-billing/understand/understand-azure-marketplace-charges?WT.mc_id=Portal-Microsoft_Azure_Support)
- Learn more on Azure CSP (Cloud Solution Provider) billing: [Azure CSP Billing and usage](https://docs.microsoft.com/partner-center/azure-plan-lp?WT.mc_id=Portal-Microsoft_Azure_Support)
- Understand daily usage: [Understand your bill for Microsoft Azure](https://docs.microsoft.com/azure/cost-management-billing/understand/review-individual-bill?WT.mc_id=Portal-Microsoft_Azure_Support)
- Manage costs: [Prevent unexpected costs with Azure billing and cost management](https://docs.microsoft.com/azure/cost-management-billing/manage/getting-started?WT.mc_id=Portal-Microsoft_Azure_Support)
