<properties
	pageTitle="add or edit vat tax id or po number"
	description="add or edit vat tax id or po number"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32632927"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="billing-addoreditvattaxidorponumber"
	ownershipId="ASMS_Billing"
/>

# Add or edit tax id, po number, sold-to or bill-to

## **Recommended Steps**

You can't update these properties on an existing invoice in the portal. The updated values are only used for invoices that are generated in the future.

## Add or edit TAX ID

The Tax ID is used for tax exemption calculation and appears on your invoice.

1. Go to the [Cost Management + Billing](https://portal.azure.com/#blade/Microsoft_Azure_GTM/ModernBillingMenuBlade/Overview) page
2. Select **Properties** from the left-hand side
3. Select **Manage Tax IDs** from the Tax IDs section, then enter your new Tax ID
4. Select **Update**

If you don't see the Tax IDs section, Tax IDs are not yet collected for your region or updating Tax IDs in the portal is not supported for your account.

## Add or edit PO number

Adding a PO number is only supported for customers who pay by invoice (Check/Wire transfer). The instructions to update PO number depend on your billing account type. To learn more about billing accounts and identify your billing account type, see [View billing accounts in Azure portal](https://docs.microsoft.com/azure/cost-management-billing/manage/view-all-accounts).

### Editing a PO number for a Microsoft Online Service Program (MOSP) billing account

You need to have an [account admin](https://docs.microsoft.com/azure/role-based-access-control/rbac-and-directory-admin-roles#classic-subscription-administrator-roles) role to edit PO number.

1. Select your subscription from the [Subscriptions page](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade)
1. Select **Payment methods** from the left-hand side
1. From the payment methods table, click on **Invoice**
1. Enter your new **PO number** and then click **Save**

### Editing a PO number for a Microsoft Customer Agreement (MCA) billing account

You need to have an owner or a contributor role on a billing profile or a billing account to update PO number.

1. Go to the [Cost Management + Billing](https://portal.azure.com/#blade/Microsoft_Azure_GTM/ModernBillingMenuBlade/Overview) page
1. Select **Invoices** from the left-hand side
1. Select **Update po number** from the Useful links section
1. Enter the new PO number
1. Select **Update**

### Editing PO numbers for Enterprise Agreement (EA) enrollments

1. Sign into [EA portal](https://ea.azure.com)
1. Select **Reports** from the left-hand side
1. Click **Usage Summary** from the top of the page
1. Select the relevant period from the dropdown
1. Select **View/Edit PO Numbers**
1. Enter the new PO number and click **Save**

## Edit sold-to and bill-to

The instructions to update sold-to and bill-to depend on your billing account type. To learn more about billing accounts and identify your billing account type, see [View billing accounts in Azure portal](https://docs.microsoft.com/azure/cost-management-billing/manage/view-all-accounts).

### Editing sold-to and bill-to for a Microsoft Online Service Program (MOSP) billing account

You need to have an [account admin](https://docs.microsoft.com/azure/role-based-access-control/rbac-and-directory-admin-roles#classic-subscription-administrator-roles) role to add or edit sold-to and bill-to.

1. Go to the [Cost Management + Billing](https://portal.azure.com/#blade/Microsoft_Azure_GTM/ModernBillingMenuBlade/Overview) page
1. Select **Properties** from the left-hand side
1. Select **Update sold to/bill to** from the Sold to/Bill to section, then enter your new address
1. Select **Save**

### Editing sold-to and bill-to for a Microsoft Customer Agreement (MCA) billing account

The tax for your Azure consumption is calculated based on your sold-to. You need to have an owner or a contributor role on a billing account to update sold-to. To update bill-to, you need to have an owner or a contributor on a billing profile or a billing account.

1. Go to the [Cost Management + Billing](https://portal.azure.com/#blade/Microsoft_Azure_GTM/ModernBillingMenuBlade/Overview) page
1. Select **Invoices** from the left-hand side
1. Select **sold-to** or **bill-to** from the Useful links section
1. Enter the new address
1. Select **Save**

### Editing sold-to and bill-to for an for Enterprise Agreement (EA) enrollment

The sold to and bill to for an Enterprise Agreement enrollment can't be updated in the portal. Please contact Azure support to update the sold to and the bill to.

## Edit subscription/ship to address for a Microsoft Online Service Program (MOSP) subscription

Address where the service is being used, usually the same as the sold-to address. The tax for your Azure consumption is calculated based on this address. You need to have an owner or a contributor role on the subscription to update its subscription address.

1. Select your subscription from the [Subscriptions page](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade).
1. Select **Properties** from the left-hand side
1. Select **Update Address** from the Subscription Address section, then enter your new address
1. Select **Save**

## **Recommended Documents**

* Check the list of supported countries/regions and currencies in the Purchase FAQ: [Supported countries/regions and currencies](https://azure.microsoft.com/pricing/faq/)
* [How to pay by Invoice](https://docs.microsoft.com/azure/billing/billing-how-to-pay-by-invoice)
* [How to add, update or remove a credit or debit card from Azure](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card)
