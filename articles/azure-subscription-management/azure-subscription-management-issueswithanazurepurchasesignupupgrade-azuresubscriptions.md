<properties
	pageTitle="purchase,signup or upgrade - unable to sign-up"
	description="purchase,signup or upgrade - unable to sign-up"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32632950"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="public,BlackForest, Fairfax, MoonCake, usnat, ussec"
	articleId="issueswithpurchasesignuporupgradeforazuresubscriptions"
	ownershipId="ASMS_SubscriptionManagement"
/>

# Purchase,signup or upgrade - unable to sign-up

## **Recommended Steps**

**Download your invoice from Azure portal (.pdf)**

* Select your subscription from the [Subscriptions page](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade) in Azure portal as [a user with access to invoices](https://docs.microsoft.com/azure/billing/billing-manage-access)
* Select **Invoices**
* Click **Download Invoice** to view a copy of your PDF invoice. If it says **Not available**, see [Why don't I see an invoice for the last billing period?](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date#noinvoice). You can also view your daily usage by clicking the billing period.
* Learn more:

   * [Download invoices for a Microsoft Customer Agreement](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date#download-your-azure-invoices-pdf)
   * Receive [Azure invoices emailed direct to your inbox](https://azure.microsoft.com/blog/azure-email-invoices/)
   * [Get invoice in email for a Microsoft Customer Agreement](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date#get-your-invoice-in-email-pdf)

**Unexpected Charges**<br>

The anniversary day is the day of the month you purchased the subscription. The invoice is generated on the anniversary date and 10 days later the credit card is charged. Invoice customers need to pay using Wire transfer/check and the details for payment is available on your monthly invoice.<br>
For example, if you purchased the subscription on January 15th, the anniversary day will be the 15th of each month when the invoice is generated and 10 days later the card is charged.<br>

**Note**: If you cancel your subscription/resource in the middle of your billing cycle, you might still see a charge which would be for any usage in the previous month. For example, if your billing cycle was from the 26th of every month to the 25th of the next month & you suspended the subscription on the 23rd, which is 28 days into the billing cycle for June, you might see a charge for the 28 days of use. 
If you see a charge in spite of cancelling a subscription please make sure, you don’t have any other support plans which is causing the charge. If you do, please go ahead and cancel the plan.<br>

**Unable to Upgrade/Sign-up/Purchase Azure**<br>

You may experience an issue when you try to sign up for a new account in the Microsoft Azure portal or Azure account center. Before you troubleshoot the issue, first consider the following suggestions:

* Make sure that the information that you provided for your Azure account profile (including contact email address, street address, and telephone number) is correct
* Make sure that the credit card information is correct
* Make sure that you don’t already have a Microsoft account that has the same information

**Unable to access services**<br>

This may be caused by a disabled subscription, due to outstanding charges. Please make sure to login as an admin to settle the payments before [reactivating the subscription](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable).

**Azure Free Trial**

Azure free trial account is only for 1 month and once it is upgraded to [Pay-as-you-go](https://azure.microsoft.com/offers/ms-azr-0003p/) there will be 12 month free services. When you upgrade from a Free Trial subscription, you keep your remaining credit for the full 30 days after you created the subscription. You also have access to free services for 12 months. If you want to [transfer the subscription](https://docs.microsoft.com/azure/billing/billing-subscription-transfer) after upgrading, you must wait until the subscription offer ID changes to MS-AZR-003P. The offer ID changes when:

* You consume all the remaining credit, or
* 30 days pass since the start of the free trial: [Products available monthly for free under Azure free account](https://azure.microsoft.com/free/free-account-faq/)
  
**Unable to create or upgrade to another support plan**

* Make sure to sign in to Azure account center as account admin. If you already have a subscription add a payment method to reactivate it. Please make sure to wait for few hours for the process completion.
* The credit card linked to the current plan might have spending limit or some other issue. Please try linking to another card.

**Note**: Support plans are billed like separate subscriptions and have subscription ID’s associated with them for billing purposes. All subscriptions on an account will receive the benefits associated with that support plan.
      
**Unable to move from one resource group to another**<br>
Only an account admin or the service administrator for the subscription can perform this action. Refer to [move resources](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources) to learn more.
		
**Azure for Students**

* Unable to sign-up for Azure for student offer: Make sure the email used for the sign-up is entitled for Azure for student and the email and is added as work or school or as Microsoft account. In case it's not added, please reach out to your local IT team to add the email in the org directory.
* Azure for Students subscription disabled due to exhausting the spending limit:

   * [Remove any spending limits](https://docs.microsoft.com/azure/billing/billing-spending-limit)
   * If you are getting an error, please [Add/Update Credit Card](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card) to your Azure Profile and convert the offer to Pay-As-You-Go

* Unable to sign-up for Azure for student offer due to error message "**You are not eligible for an Azure subscription**":<br>
This could be due to an unmanaged Active Directory tenant issue. Please follow the steps below:

   * Open an InPrivate session of Internet Explorer and go to [Azure for Students](https://imagine.microsoft.com/azure)
   * Log in using your Microsoft Personal Account (if you don't have one, create it from [create account](http://signup.live.com))
   * Complete the verification process using your Microsoft School Account address or activation code
   * Continue the activation of the Azure plan using the Microsoft Personal Account
   
**Encountering browser issues  (Browser hangs, keeps spinning, does not load, etc.)**<br>

**Note**: You might be affected by an outage. Please check to see if there is an on-going outage: [Azure Health Status](https://status.azure.com/status/history/).

**Page hangs in the loading status**<br>
If your internet browser page hangs, try each of the following steps until you can get to the Azure portal:

   * Refresh the page
   * Use a different internet browser
   * Use the private browsing mode for your browser. For Internet Explorer: Click **Tools > Safety > InPrivate Browsing**, and then browse and sign-in to the [Azure portal](https://portal.azure.com/) or [Azure account center](https://account.azure.com/Subscriptions).

**You are automatically signed in as a different user**<br>

This issue can occur if you use more than one user account in an internet browser. Learn more: [Troubleshoot Sign-in Issues](https://support.microsoft.com/help/4042961/troubleshoot-why-you-can-t-sign-in-to-manage-your-azure-subscription).

**Unable to access subscriptions**<br>

* In the [Azure portal](https://portal.azure.com/), make sure that the correct Azure directory is selected from the account at the top right
* In the [Azure Account center](https://account.windowsazure.com/Subscriptions), make sure if the account used is the account admin<br>
Learn more: [Troubleshoot No Subscriptions found](https://docs.microsoft.com/azure/billing/billing-no-subscriptions-found)<br>

## **Recommended Documents**

* [How to download your invoice and usage data](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date)
* [How to request copy of Azure invoice via email](https://azure.microsoft.com/blog/azure-email-invoices/)
* [Troubleshoot issues signing up for Azure](https://docs.microsoft.com/azure/billing/billing-troubleshoot-azure-sign-up-issues/)
* [Manage (Reactivate/cancel/Switch) subscription](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable)
* [How to Edit profile](https://docs.microsoft.com/azure/billing/billing-how-to-change-azure-account-profile)
* [Understand terms on your invoice](https://docs.microsoft.com/azure/billing/billing-understand-your-invoice)
* Manage payment - [Update, change, or remove payment methods](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card)
* [Activate monthly Azure credit for Visual Studio subscribers](https://azure.microsoft.com/pricing/member-offers/msdn-benefits/)
* [Microsoft Partner Network (MPN) - Benefits, requirements, enroll, and manage](https://partner.microsoft.com/membership/core-benefits#Core%20benefits)
* [Migrate resources between accounts/subscriptions](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)
* [Add/Manage admins and co-admins](https://docs.microsoft.com/azure/billing/billing-add-change-azure-subscription-administrator)
