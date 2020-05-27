<properties
	pageTitle="reserved instance - issue not listed"
	description="reserved instance - issue not listed"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32690276"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="public,BlackForest, Fairfax, MoonCake, usnat, ussec"
	articleId="08b1aa47-f908-41af-b3eb-37c6e45d3dcd"
	ownershipId="ASMS_SubscriptionManagement"
/>

# Reserved instance - issue not listed

## **Recommended Steps**

**Check if you are impacted by an outage**: [Azure Health Status](https://status.azure.com/status)<br>

**How is reservation discount applied to existing resources?**<br>

Reservation benefit automatically applies to existing resources that match the reservation SKU, region and scope. There is no tagging of a reservation to a resource. [Learn more](https://docs.microsoft.com/azure/cost-management-billing/reservations/save-compute-costs-reservations#how-reservation-discount-is-applied)<br>

**Self-service exchanges and refunds for Azure Reservations**<br>

* You can exchange a reservation for another reservation of the same type. You can also refund a reservation, up to $50,000 USD per year, if you no longer need it.
* It is possible to exchange multiple low cost reservations with one equal or greater costing reservation if the price of new RI is equal or greater. It is only possible to Exchange multiple RIs for 1 new RI in one transaction<br>
* If a reservation is transferred from one subscription to another there will be no change in reservation expiry date<br>
* If the refund amount for the reservation is more than $50,000 USD, the self-serve exchange option is unavailable. A support ticket needs to be created for this request and it will be reviewed by the support team and the possible options would be shared<br>

Learn more: [Cancel, exchange or refund reservations](https://docs.microsoft.com/azure/billing/billing-azure-reservations-self-service-exchange-and-refund)<br>

**Purchase a Reserved Instance**<br>

Purchases of RI are only supported under **Pay-As-You-Go (3P)** and **Enterprise Agreement (17P)** offer types<br>

**Note**: You must be in the role **Owner** on the subscription to buy a Reserved Instance. For purchasing reservations in an enterprise enrollment, the enterprise administrator must enable reservation purchases in the EA portal, by default the setting is enabled for all enrollments.<br>

Before purchasing, please check if the RI is supported for the region you are purchasing since if capacity is unavailable for a region, you will not be able to purchase RI in that region.<br>

Reserved Instance for Pay-As-You-Go is **not** available in the following countries: Brazil, India, China, Taiwan, Russia, Korea, Argentina, Hong Kong, Indonesia,  Liechtenstein,  Malaysia, Mexico, Saudi Arabia, South Africa, Turkey. Refer to [Products available by region](https://azure.microsoft.com/global-infrastructure/services/) for more information.

<**Unable to see the reservation after creation**<br>

You might be unable to see the Reserved Instances due to a missing RBAC role that is necessary to have full access to the desired Instances. Please reach out to the Account Administrator of the subscriptions that have the Reserved Instances to follow below steps:

1. Sign in to the [Azure portal](https://portal.azure.com/)<br>
2. Select **All Services > Reservation** to list reservations that you have access to<br>
3. Select the reservation that you want to delegate access to other users<br>
4. Select **Access control (IAM)**<br>
5. Select **Add role assignment > Role > Owner**. Or, if you want to give limited access, select a different role.
6. Type the email address of the user you want to add as owner<br>
7. Select the user, and then select **Save**<br>

Learn more: [Manage Reservations](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance)<br>

The Enterprise Administrator can transfer ownership of subscriptions within an enrollment. To learn more see [Transfer Account Ownership in the EA portal](https://docs.microsoft.com/azure/cost-management-billing/manage/ea-portal-administration#transfer-enterprise-enrollment-to-a-new-one).

**Troubleshoot Browser issues (Browser hangs, keeps spinning, does not load, etc.)**<br>

**Unable to access subscriptions (Incorrect directory selected)**<br>

* In the [Azure portal](https://portal.azure.com/), make sure that the correct Azure directory is selected from the account at the top right
* In the [Azure Account center](https://account.windowsazure.com/Subscriptions), make sure if the account used is the account admin
* Learn more: [Troubleshoot No Subscriptions found](https://docs.microsoft.com/azure/billing/billing-no-subscriptions-found)

**Page hangs in the loading status**<br>
If your internet browser page hangs, try each of the following steps until you can get to the Azure portal<br>

* Refresh the page
* Use a different internet browser
* Use the private browsing mode for your browser. For Internet Explorer: Click **Tools > Safety > InPrivate Browsing**, and then browse and sign-in to the [Azure portal](https://portal.azure.com/) or [Azure Account center](https://account.windowsazure.com/Subscriptions).

**You are automatically signed in as a different user**<br>
This issue can occur if you use more than one user account in an internet browser.To resolve the issue, try one of the following methods:<br>

* Clear the cache and delete Internet cookies. In Internet Explorer, click **Tools > Internet Options > Delete**. Make sure that the check boxes for temporary files, cookies, password, and browsing history are selected, and then click Delete
* Reset the Internet Explorer settings to revert any personal settings that you’ve made. Click **Tools > Internet Options > Advanced** > select the **Delete personal settings** box > **Reset**
* Use the private browsing mode for your browser. For Internet Explorer: Click **Tools > Safety > InPrivate Browsing**, and then browse and sign-in to the [Azure portal](https://portal.azure.com/) or [Azure Account center](https://account.windowsazure.com/Subscriptions).

Learn more: [Troubleshoot Sign-in Issues](https://support.microsoft.com/help/4042961/troubleshoot-why-you-can-t-sign-in-to-manage-your-azure-subscription)<br>

**Azure Free Account**<br>
The Azure Free Account offer includes $200 of Azure credits (to be used within the first 30 days of sign-up) and 12 months of select free services (subject to change).<br>
This offer is limited to one enrollment per eligible customer and cannot be combined with any other offer unless otherwise permitted by Microsoft.<br>
Within 30 days of sign-up or upon exhaustion of the customer’s credits (whichever occurs first), the customer must upgrade to a Pay-As-You-Go account by removing the Spending Limit. This allows continued use of the Azure Free Account for the remaining 11 months. After the customer has upgraded, usage outside the initial credits and select free services will be billed at Pay-As-You-Go rates. If the customer elects not to upgrade, the Free Account subscription will be disabled.<br>

Learn more: [Products available monthly for free under Azure free account](https://azure.microsoft.com/free/free-account-faq/)<br>
Additional FAQ: [Free account FAQ](https://azure.microsoft.com/free/free-account-faq/)<br>

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
