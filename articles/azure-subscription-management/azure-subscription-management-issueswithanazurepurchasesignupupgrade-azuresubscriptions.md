<properties
	pageTitle="issues with purchase, signup or upgrade for azure subscriptions"
	description="issues with purchase, signup or upgrade for azure subscriptions"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32632950,32632948,32632955"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="public"
	articleId="issueswithpurchasesignuporupgradeforazuresubscriptions"
/>

# issues with purchase, signup or upgrade for azure subscriptions

* [Azure subscriptions](https://docs.microsoft.com/azure/architecture/aws-professional/) are a grouping of resources with an assigned owner responsible for billing and permissions management. Subscriptions exist independently of their owner accounts, and can be reassigned to new owners as needed. [Azure Offers](https://azure.microsoft.com/support/legal/offer-details/)<br>
* [Azure Services](https://azure.microsoft.com/services/) is an example of a platform as a service (PaaS). It is designed to support applications that are scalable, reliable, and inexpensive to operate.<br>
* [Azure Marketplace](https://azuremarketplace.microsoft.com/) is the premier destination for all software needs, certified and optimized to run on Azure. Learn more: [Azure marketplace apps](https://azuremarketplace.microsoft.com/marketplace/apps)<br>


### Unable to Sign-up/Purchase Azure

You may experience an issue when you try to sign up for a new account in the Microsoft Azure portal or Azure account center. Before you troubleshoot the issue, first consider the following suggestions:

* Make sure that the information that you provided for your Azure account profile (including contact email address, street address, and telephone number) is correct
* Make sure that the credit card information is correct
* Make sure that you don’t already have a Microsoft account that has the same information.

### **Unable to access services**
Could be since the subscription is disabled due to outstanding charges. Please make sure to login as an admin to settle the payments before [reactivating the subscription](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable)

### **Azure Free Trial**
The Azure Terms of Use agreement limits free trial activation only for a user that's new to Azure. If you have had any other type of Azure subscription, you can't activate a free trial. Consider signing up for a [Pay-As-You-Go subscription](https://azure.microsoft.com/offers/ms-azr-0003p/)

* Free trial suspended due to expiration (sponsorship end date)

	* Convert to [Pay-as-you-go](https://azure.microsoft.com/offers/ms-azr-0003p/) to continue to have access to the selected free services for the remaining 12- month duration of that offer. If you are not the admin, reach out to support and provide an approval email from the account admin<br>
	* Convert to [Azure for students](https://azure.microsoft.com/offers/ms-azr-0170p/)<br>
	
* Unable to create/ upgrade to another support plan

	* Make sure to sign in to Azure account center as account admin. If you already have a subscription add a payment method to re-activate it. Please make sure to wait for few hours for the process completion<br>
	* The credit card linked to the current plan might have spending limit on or some issue. Please try linking to another card<br>
	**Note**: Support plans are billed like separate subscriptions and have subscription ID’s associated with them for billing purposes. All subscriptions on an account will receive the benefits associated with that support plan

* Unable to move one resource group to another

	* Only an account admin or the service administrator for the subscription can perform this action. Refer [move resources](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources) to learn more
		
### **Azure for Students**

* Azure for Students subscription disabled due to exhausting the spending limit<br>

	* [Remove any spending limit](https://docs.microsoft.com/azure/billing/billing-spending-limit.)<br>
	* If you are getting an error please [add/Update Credit Card](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card.) to your Azure Profile and convert the offer to Pay-As-You-Go<br>
	
* Unable to sign-up for Azure for student offer<br>

	* Make sure the email used for the sign-up is entitled for Azure for student and the email and is added as work or school or as Microsoft account. In case it's not added, please reach out to your local IT team to add the email in the org directory<br>
	
* Unable to sign-up for Azure for student offer due to error message **"You are not eligible for an Azure subscription"**
This could be due to an unmanaged Active Directory tenant issue. Please follow the steps below

	* Open an InPrivate session of Internet Explorer and go to [Azure for Students](https://imagine.microsoft.com/azure)<br>
	* Log in using your Microsoft Personal Account (if you don't have one, create it from create account)<br>
	* Complete the verification process using your Microsoft School Account address or activation code<br>
	* Continue the activation of the Azure plan using the Microsoft Personal Account<br>

### **Encountering browser issues**

* Please log out of all the active azure sessions. Follow the below steps [here](http://www.thewindowsclub.com/launch-start-private-browsing) for in- Private session of the internet explorer, if using google chrome please use the incognito mode of the browsing
* You could also try to Refresh browser, use another browser, delete cache cookies if above doesn't work. Learn more: [Troubleshoot Sign-up Issues](https://support.microsoft.com/help/4467267/can-t-sign-up-for-azure-in-azure-portal-or-azure-account-center)


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

