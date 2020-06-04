<properties
	pageTitle="cancel subscriptions-issue not listed"
	description="cancel subscriptions-issue not listed"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32680688"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="cancelswitchorreenablesubscriptions-issue not listed"
	ownershipId="ASMS_SubscriptionManagement"
/>

# Cancel Subscription-issue not listed

**Azure for Students (170p)** is a special offer that will be available only for students that are 18 years of age or older and attend an accredited, degree-granting four-year educational institution as a full-time student or faculty in a STEM-related field. It is an addition (not a replacement) to [Azure for Students Starter (formerly Imagine) subscription](https://internal.support.services.microsoft.com/help/3048361/azure-support---imagine-formally-known-as-dreamspark). This offer consists of a $100 USD credit (provided via Sponsorship benefit) that can be used for 12 months and Free Services equal to the ones available on Free Account.<br>

* [Azure for Students FAQ](https://azure.microsoft.com/free/free-account-students-faq/)
* [Contact Sales team](https://azure.microsoft.com/overview/sales-number/)

**Azure CSP**

  * [Add an Azure CSP Subscription](https://docs.microsoft.com/azure/cloud-solution-provider/integration/manage-customers/add-subscriptions)
  * [Available Azure services in Azure CSP](https://docs.microsoft.com/azure/cloud-solution-provider/overview/azure-csp-available-services)
  * [Azure Marketplace items in Azure CSP](https://docs.microsoft.com/azure/cloud-solution-provider/overview/azure-csp-available-services#azure-marketplace-items-in-azure-csp)
  * [Azure partner shared services](https://docs.microsoft.com/azure/cloud-solution-provider/overview/partner-shared-services)
  * [Azure subscription migration](https://docs.microsoft.com/azure/cloud-solution-provider/migration/migration?tabs=ea-to-csp)

Subscription ownership transfers are only allowed if the subscription is being transferred from one CSP partner to another CSP partner. Offer conversions are not supported for this offer.<br>
[CSP- Billing FAQ](https://docs.microsoft.com/partner-center/faq-about-new-billing-features)

## **Recommended Steps**

### **Delete/Deprovision subscription**

You can cancel, change, or re-enable your Azure subscription as the [Account Administrator](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#whoisaa). If you are not the AA, before a subscription can be deprovisioned:

  * A written (email) approval from the Account Administrator (AA) must be obtained
  * The AA must acknowledge that they understand all data will be permanently deleted
  * If you are unable to do the above, follow [Subscription ownership transfer](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)
  * Justification for deprovisioning
  * The subscription should already be SUSPENDED. The only exception is if the account is inaccessible, preventing you from suspending the subscription. 
  
**Note**: Deprovisioning is an irreversible action. Once the process has been executed all date will be lost.

### **Move Resources**

Azure resources can be moved to either another Azure subscription or another resource group under the same subscription. You can use the Azure portal, Azure PowerShell, Azure CLI, or the REST API to move resources. Moving a resource only moves it to a new resource group or subscription. It doesn't change the location of the resource.

  * Learn more: [Move resources to a new resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)
  * Learn more: [Checklist before moving resources](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources#checklist-before-moving-resources)
  * Learn more: [Tutorial: Move Azure resources to another resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-tutorial-move-resources)
  * Learn more: [Services that can be moved](https://docs.microsoft.com/azure/azure-resource-manager/move-support-resources)

**Note**: If you want to upgrade your Azure subscription (such as switching from free to pay-as-you-go), you need to convert your subscription.

  * To upgrade a free trial: [Upgrade your Azure subscription](https://docs.microsoft.com/azure/billing/billing-upgrade-azure-subscription)
  * To change a pay-as-you-go subscription: [Switch subscription offer](https://docs.microsoft.com/azure/billing/billing-how-to-switch-azure-offer)

### **Azure Free Trial**

You can upgrade your [Free Trial](https://azure.microsoft.com/free/) or [Microsoft Imagine](https://azure.microsoft.com/offers/ms-azr-0144p/) subscription to [Pay-As-You-Go](https://azure.microsoft.com/offers/ms-azr-0003p/) in the Azure Account Center:

* Sign in to the [Azure Account Center](https://account.windowsazure.com/subscriptions)
* In the subscription status section, click the **Upgrade now** banner
* Confirm your upgrade

Learn more: [Upgrade Subscription](https://docs.microsoft.com/azure/billing/billing-upgrade-azure-subscription)

**Note**: Azure free trial account is only for 1 month and once it is upgraded to pay-g there will be 12 month free services. When you upgrade from a Free Trial subscription, you keep your remaining credit for the full 30 days after you created the subscription. You also have access to free services for 12 months. If you want to [transfer the subscription](https://docs.microsoft.com/azure/billing/billing-subscription-transfer) after upgrading, you must wait until the subscription offer ID changes to MS-AZR-003P. The offer ID changes when:

* You consume all the remaining credit, or
* 30 days pass since the start of the free trial

[Products available monthly for free under Azure free account](https://azure.microsoft.com/free/free-account-faq/)<br>

Additional FAQ: [Free account FAQ](https://azure.microsoft.com/free/free-account-faq/)

## **Recommended Documents**

* [Cancel subscription](https://docs.microsoft.com/azure/billing/billing-how-to-cancel-azure-subscription)
* [Reactivate subscription](https://docs.microsoft.com/azure/billing/billing-how-to-cancel-azure-subscription#reactivate-subscription)
* [Switch subscription](https://docs.microsoft.com/azure/billing/billing-how-to-switch-azure-offer)
* [Azure Marketplace](https://azuremarketplace.microsoft.com/marketplace/?source=datamarket)
* [How to download your invoice and usage data](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date)
* [How to request copy of Azure invoice via email](https://azure.microsoft.com/blog/azure-email-invoices/)
* [Migrate resources between accounts/subscriptions](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)
* [Add/Manage admins and co-admins](https://docs.microsoft.com/azure/billing/billing-add-change-azure-subscription-administrator)
* Locate the [Account Admin](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#whoisaa)
* [What do I do if my Azure subscription becomes disabled? ](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable/)
* [Azure spending limit](https://docs.microsoft.com/azure/cost-management-billing/manage/spending-limit)
