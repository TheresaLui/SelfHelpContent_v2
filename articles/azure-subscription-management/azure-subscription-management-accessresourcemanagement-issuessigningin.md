<properties
	pageTitle="issues signing in or accessing my subscription"
	description="issues signing in or accessing my subscription"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32632953"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="public,BlackForest, Fairfax, MoonCake, usnat, ussec"
	articleId="accessandresourcemanagementissuessigninginoraccessingmysubscription"
	ownershipId="ASMS_SubscriptionManagement"
/>

# issues signing in or accessing my subscription

### **Awareness**
If you are experiencing location constraint, please try alternate regions (as first preference) since the location might not be available at this unprecedented time. Please review our [commitment to customers and Microsoft Cloud Services continuity](https://azure.microsoft.com/blog/our-commitment-to-customers-and-microsoft-cloud-services-continuity/) for more details about this capacity constraint. For additional questions about this, contact support by selecting the below path only:<br>

* **Issue type**: Service and subscription limits (quotas)
* **Quota type**: Compute-VM (cores-vCPUs) subscription limit increases

## Recommended Steps

### **Unable to Sign-in Azure due to browser issues (Browser hangs, keeps spinning, does not load, etc.)**

* You might be impacted by an outage. Please check to see if there is an ongoing outage: [Azure Health Status](https://status.azure.com/status/history/)<br>
* Please log out of all the active azure sessions. Follow the below steps [here](http://www.thewindowsclub.com/launch-start-private-browsing) for in- Private session of the internet explorer, if using google chrome please use the incognito mode of the browsing<br>
* You could also try to Refresh browser, use another browser, delete cache cookies if above doesn't work<br>
	
Learn more: [Troubleshoot Sign-in Issues](https://support.microsoft.com/help/4042961/troubleshoot-why-you-can-t-sign-in-to-manage-your-azure-subscription)

### **Unable to access subscriptions**

* In the [Azure portal](https://portal.azure.com/), make sure that the correct Azure directory is selected from the account at the top right
* In the [Azure Account center](https://account.windowsazure.com/Subscriptions), make sure if the account used is the account admin

Learn more: [Troubleshoot No Subscriptions found](https://docs.microsoft.com/azure/billing/billing-no-subscriptions-found)
	
### **Unable to access billing history**

* The account admin needs to make sure the user accessing the billing information is added in the Azure Active directory as a guest user: [Add or delete a new user](https://docs.microsoft.com/azure/active-directory/fundamentals/add-users-azure-active-directory)<br>
* The user then needs to be given a Global admin role: [Assign role to users](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal)<br>
* Post this, the user can be given billing access using RBAC policies: [Grant access to billing](https://docs.microsoft.com/azure/billing/billing-manage-access)<br>

The **Azure Free Account** offer includes $200 of Azure credits (to be used within the first 30 days of sign-up) and 12 months of select free services (subject to change).
This offer is limited to one enrollment per eligible customer and cannot be combined with any other offer unless otherwise permitted by Microsoft.<br>
Within 30 days of sign-up or upon exhaustion of the customer’s credits (whichever occurs first), the customer must upgrade to a Pay-As-You-Go account by removing the Spending Limit. This allows continued use of the Azure Free Account for the remaining 11 months. After the customer has upgraded, usage outside the initial credits and select free services will be billed at Pay-As-You-Go rates. If the customer elects not to upgrade, the Free Account subscription will be disabled.<br>
Learn more : [Products available monthly for free under Azure free account](https://azure.microsoft.com/free/free-account-faq/)

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
