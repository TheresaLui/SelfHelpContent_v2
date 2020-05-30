<properties
	pageTitle="reserved instance-blade issues"
	description="reserved instance-blade issues"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32680693"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="public,BlackForest, Fairfax, MoonCake, usnat, ussec"
	articleId="reservedinstance-bladeissues"
	ownershipId="ASMS_SubscriptionManagement"
/>

# reserved instance-blade issues

## **Recommended Steps**

### Unable to see the reservation after creation

You might be unable to see the Reserved Instances due to a missing RBAC role that is necessary to have full access to the desired Instances. Please reach out to the Account Administrator of the subscriptions that have the Reserved Instances to follow below steps:

1. Sign in to the [Azure portal](https://portal.azure.com/)<br>
2. Select **All Services > Reservation** to list reservations that you have access to<br>
3. Select the reservation that you want to delegate access to other users<br>
4. Select **Access control (IAM)**<br>
5. Select **Add role assignment > Role > Owner**. Or, if you want to give limited access, select a different role.
6. Type the email address of the user you want to add as owner<br>
7. Select the user, and then select **Save**<br>

### Reserved Instance return/exchange error

To perform an exchange or refund, the user must have access to the reservation order. When granting someone permissions, it’s best to grant permissions to the reservation order, not the reservation. If you are unable to perform exchange/return, you might not have the right admin permissions. Please reach to the admin of the reservations to give you the admin access in order to perform the actions successfully.<br>

* [Add/change users who can manage a reservation](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance#add-or-change-users-who-can-manage-a-reservation)

### Troubleshoot Browser issues (Browser hangs, keeps spinning, does not load, etc.)

Note: You might be affected by an outage. Please check to see if there is an on-going outage: [Azure Health Status](https://status.azure.com/status/history/)

### Page hangs in the loading status
If your internet browser page hangs, try each of the following steps until you can get to the Azure portal:

* Refresh the page
* Use a different internet browser
* Use the private browsing mode for your browser. For Internet Explorer: Click **Tools > Safety > InPrivate Browsing**, and then browse and sign-in to the [Azure portal](https://portal.azure.com/) or [Azure account center](https://account.azure.com/Subscriptions).

### You are automatically signed in as a different user
This issue can occur if you use more than one user account in an internet browser. To resolve the issue, try one of the following methods:

* Clear the cache and delete Internet cookies. In Internet Explorer, click **Tools > Internet Options > Delete**. Make sure that the check boxes for temporary files, cookies, password, and browsing history are selected, and then click Delete.
* Reset the Internet Explorer settings to revert any personal settings that you’ve made. Click **Tools > Internet Options > Advanced**> select the **Delete personal settings** box > **Reset**.
* Use the private browsing mode for your browser. For Internet Explorer: Click **Tools > Safety > InPrivate Browsing**, and then browse and sign-in to the [Azure portal](https://portal.azure.com/) or [Azure account center](https://account.azure.com/Subscriptions).

* [Troubleshoot Sign-in Issues](https://support.microsoft.com/help/4042961/troubleshoot-why-you-can-t-sign-in-to-manage-your-azure-subscription)<br>

### Unable to access subscriptions

* In the [Azure portal](https://portal.azure.com/), make sure that the correct Azure directory is selected from the account at the top right
* In the [Azure Account center](https://account.windowsazure.com/Subscriptions), make sure if the account used is the account admin

* [Troubleshoot No Subscriptions found](https://docs.microsoft.com/azure/billing/billing-no-subscriptions-found)

## **Recommended Documents**

* [Azure Reserved VM Instances - FAQ](https://azure.microsoft.com/pricing/reserved-vm-instances/#faq)
* [Azure Pricing](https://azure.microsoft.com/pricing/reserved-vm-instances/)
* [Azure Purchase FAQ](https://azure.microsoft.com/pricing/faq/)
* [Prepay for Virtual Machines with reserved instances](https://docs.microsoft.com/azure/virtual-machines/windows/prepay-reserved-vm-instances)
* [Understand how the reserved instance discount is applied](https://docs.microsoft.com/azure/billing/billing-understand-vm-reservation-charges)
* [Save money on virtual machines with Azure Reserved Instances](https://docs.microsoft.com/azure/billing/billing-save-compute-costs-reservations)
* [Understand reserved instance usage for your Pay-As-You-Go subscription](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage)
* [Understand reserved instance usage for your Enterprise enrollment](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage-ea)
* [Windows software costs not included with reserved instances](https://docs.microsoft.com/azure/billing/billing-reserved-instance-windows-software-costs)
* [Manage reserved instances](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance)
* [Manage Microsoft Azure reservations on behalf of your customers](https://docs.microsoft.com/partner-center/azure-reservations-manage)
* [Reserved instances in Partner Center Cloud Solution Provider (CSP) program](https://docs.microsoft.com/partner-center/azure-reservations)
