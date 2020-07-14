<properties
	pageTitle="Access resources-issue not listed"
	description="Access resources-issue not listed"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32680689"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="public,BlackForest, Fairfax, MoonCake, usnat, ussec"
	articleId="accessresources-issue not listed"
	ownershipId="ASMS_SubscriptionManagement"
/>
 
# Access resources-issue not listed

## **Recommended Steps**

**Unable to Sign-in Azure due to browser issues (Browser hangs, keeps spinning, does not load, etc.)**

i. You might be affected by an outage. Please check to see if there is an on-going outage: [Azure Health Status](https://status.azure.com/status/history/)
ii. Please log out of all the active azure sessions. Follow the below steps [here](http://www.thewindowsclub.com/launch-start-private-browsing) for in- Private session of the internet explorer, if using google chrome please use the incognito mode of the browsing.
iii. You could also try to Refresh browser, use another browser, delete cache cookies if above doesn't work<br>
Learn more: [Troubleshoot Sign-in Issues](https://support.microsoft.com/help/4042961/troubleshoot-why-you-can-t-sign-in-to-manage-your-azure-subscription)

**Unable to access subscriptions - "No subscriptions found" error**

* In the [Azure portal](https://portal.azure.com/), make sure that the **correct Azure directory** is selected from the account at the top right
* In the [Azure Account center](https://account.windowsazure.com/Subscriptions), make sure if the account used is the account admin<br>
Learn more: [Troubleshoot No Subscriptions found](https://docs.microsoft.com/azure/billing/billing-no-subscriptions-found)
	
**Unable to access billing history**

* The account admin needs to make sure the user accessing the billing information is added in the Azure Active directory as a guest user : [Add or delete a new user](https://docs.microsoft.com/azure/active-directory/fundamentals/add-users-azure-active-directory). The user then needs to be given a Global admin role: [Assign role to users](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal)
* Post this, the user can be given billing access using RBAC policies: [Grant access to billing](https://docs.microsoft.com/azure/billing/billing-manage-access)<br>

The **Azure Free Account** offer includes $200 of Azure credits (to be used within the first 30 days of sign-up) and 12 months of select free services (subject to change).<br>
This offer is limited to one enrollment per eligible customer and cannot be combined with any other offer unless otherwise permitted by Microsoft.
Within 30 days of sign-up or upon exhaustion of the customer’s credits (whichever occurs first), the customer must upgrade to a Pay-As-You-Go account by removing the Spending Limit. This allows continued use of the Azure Free Account for the remaining 11 months. After the customer has upgraded, usage outside the initial credits and select free services will be billed at Pay-As-You-Go rates. If the customer elects not to upgrade, the Free Account subscription will be disabled.<br>
Learn more : [Products available monthly for free under Azure free account](https://azure.microsoft.com/free/free-account-faq/)<br>

**Re-enable subscription**<br>
Your Azure subscription can get disabled because your credit has expired, you reached your spending limit, have an overdue bill, hit your credit card limit, or because the subscription was canceled by the Account Administrator. Refer below on how you can re-enable your subscription<br>
Learn more: [Reactivate Azure subscription](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable)<br>

**Expired credit card**<br>
When you sign up for an Azure free account, you get a Free Trial subscription, which provides you $200 in Azure credits for 30 days and 12 months of free services. At the end of 30 days, Azure disables your subscription. Your subscription is disabled to protect you from accidentally incurring charges for usage beyond the credit and free services included with your subscription. To continue using Azure services, you must [upgrade your subscription](https://docs.microsoft.com/azure/billing/billing-upgrade-azure-subscription). After you upgrade, your subscription still has access to free services for 12 months. You only get charged for usage beyond the free services and quantities.<br>
Learn more: [Expired credit card](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable#your-credit-is-expired)<br>

**Spending Limit reached**<br>
When your usage reaches the spending limit, Azure disables your subscription for the remainder of that billing period. Your subscription is disabled to protect you from accidentally incurring charges for usage beyond the credit included with your subscription. To remove your spending limit, see [Remove the spending limit in Account Center](https://docs.microsoft.com/azure/billing/billing-spending-limit#remove).<br>
Learn more: [Reached your spending limit](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable#you-reached-your-spending-limit)<br>

**Bill past due**<br>
To resolve past due balance, see [Resolve past due balance for your Azure subscription after getting an email from Azure](https://docs.microsoft.com/azure/billing/billing-azure-subscription-past-due-balance).<br> 

**Bill exceeds your credit card limit**<br>
To resolve this issue, [switch to a different credit card](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card). Or if you're representing a business, you can [switch to pay by invoice](https://docs.microsoft.com/azure/billing/billing-how-to-pay-by-invoice).

## **Recommended Documents**

* [Add or change Azure subscription administrators](https://docs.microsoft.com/azure/billing/billing-add-change-azure-subscription-administrator)
* [Manage access using RBAC and Azure portal](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal)
