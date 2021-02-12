<properties
	pageTitle="purchase,sign up or upgrade - browser issues"
	description="purchase,sign up or upgrade - browser issues"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32680692"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="public,BlackForest, Fairfax, MoonCake, usnat, ussec"
	articleId="issueswithpurchasesignuporupgrade-browserissues"
	ownershipId="ASMS_SubscriptionManagement"
/>

# Purchase,sign up or upgrade - browser issues

## **Recommended Steps**

**Unable to Sign-in Azure due to browser issues (Browser hangs, keeps spinning, does not load, etc)**

* You might be affected by an outage. Please check to see if there is an ongoing outage: [Azure Health Status](https://status.azure.com/status/history/)
* Please log out of all the active azure sessions. Follow the below steps [here](http://www.thewindowsclub.com/launch-start-private-browsing) for in- Private session of the internet explorer, if using google chrome please use the incognito mode of the browsing
* You could also try to Refresh browser, use another browser, delete cache cookies if above doesn't work<br>
	
Learn more: [Troubleshoot Sign-in Issues](https://support.microsoft.com/help/4042961/troubleshoot-why-you-can-t-sign-in-to-manage-your-azure-subscription)<br>

**Unable to access subscriptions - "No subscriptions found" error**

* In the [Azure portal](https://portal.azure.com/), make sure that the correct Azure directory is selected from the account at the top right
* In the [Azure Account center](https://account.windowsazure.com/Subscriptions), make sure if the account used is the account admin

Learn more: [Troubleshoot No Subscriptions found](https://docs.microsoft.com/azure/billing/billing-no-subscriptions-found)<br>
	
**Unable to access billing history**<br>

* The account admin needs to make sure the user accessing the billing information is added in the Azure Active directory as a guest user : [Add or delete a new user](https://docs.microsoft.com/azure/active-directory/fundamentals/add-users-azure-active-directory)
* The user then needs to be given a Global admin role: [Assign role to users](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal)
* Post this, the user can be given billing access using RBAC policies: [Grant access to billing](https://docs.microsoft.com/azure/billing/billing-manage-access)

**Quota Increase**: For whitelisting request, please select the below to log a case<br>
**Issue Type**: Service and subscription limits (quotas)<br>
**Quota Type**: Compute-VM (cores-vCPUs) subscription limit increases<br>

**Payments with credit/debit card**

* In order to be able to make immediate payment, please make sure to [resolve past due balances](https://docs.microsoft.com/azure/billing/billing-azure-subscription-past-due-balance). If your payment isn't received or if we can't process your payment, you might get an email or see a Past due balance notification alert in the Account Center or Azure portal
* The payment may have failed to process if the credit card on file has expired or the charge was declined by your bank. The [Account Admin](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#whoisaa) can review and update the credit card in the Account Center: [Add/Update my payment method](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card)
* You might have your Azure subscription disabled because your credit is expired, you reached your spending limit, have an overdue bill, hit your credit card limit, or because the subscription was canceled by the Account Administrator. Follow the steps in the article below to get your subscription reactivated: [Reactivate my subscription](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable)
* **Declined payment**: Please make sure which payment instrument (PI) is getting declined incase you have multiple PI's associated to a subscription. If needed, change the PI by following the steps here: [How to change your credit card](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card)
* **Remove card**: If you need to remove your PI from the subscription, please follow the steps here: [Remove your credit card from the account](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card#remove-a-credit-card-from-the-account)
* If there is a pending payment on the card since the card was denied by your **financial institution**, please reach out to your financial institution to resolve the issue. Use the below pointers

   * You might have to check with the bank to see if the international transaction is enabled on the card
   * If card has credit limit to settle the balance
   * If recurring payment is enabled on the card

Check the [Payment FAQ](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card#frequently-asked-questions) to see if it resolves your issue 

## **Recommended Documents**

* [I can't sign in to manage my Azure subscription](https://docs.microsoft.com/azure/billing-cannot-login-subscription)
* [How to download your invoice and usage data](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date)
* [How to request copy of Azure invoice via email](https://azure.microsoft.com/blog/azure-email-invoices)
* [How to add, update or remove a credit or debit card from Azure](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card)
* [Manage (Reactivate/Cancel/Switch) subscription](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable)
* [How to edit your Azure account profile](https://docs.microsoft.com/azure/billing/billing-how-to-change-azure-account-profile)
* [Add/Manage admins and co-admins](https://docs.microsoft.com/azure/billing/billing-add-change-azure-subscription-administrator)
* [Azure CSP Billing/Usage](https://docs.microsoft.com/azure/cloud-solution-provider/billing/azure-csp-billing-overview)
* [Migrate resources between accounts/subscriptions](https://docs.microsoft.com/azure/cloud-solution-provider/billing/azure-csp-billing-overview)
