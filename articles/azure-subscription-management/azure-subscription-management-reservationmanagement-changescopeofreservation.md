<properties
	pageTitle="change scope of reservation"
	description="change scope of reservation"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32593232"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="public, Mooncake"
	articleId="2ab6a0c4-21ea-49f0-a88c-60597e4e38a3"
/>

# Change scope of reservation

## **Recommended Steps**

1. Sign in to the [Azure portal](https://portal.azure.com/)
2. Select **All services > Reservations**
3. Select the reservation
4. Select **Settings > Configuration**
5. Change the scope

If the scope is changed from shared to single scope, only select subscriptions where you are the owner can be selected. Only subscriptions within the same billing context as the reservation, can be selected. The scope only applies to Pay-As-You-Go offer MS-AZR-0003P or MS-AZR-0023P, Enterprise offer MS-AZR-0017P or MS-AZR-0148P, or CSP subscription types.<br>

Learn more: [Change reservation scope](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance#change-the-reservation-scope)<br>

The Enterprise Administrator can transfer ownership of subscriptions within an enrollment. To learn more see [Transfer Account Ownership](https://ea.azure.com/helpdocs/changeAccountOwnerForASubscription) in the EA portal. 

### Reserved Instance Exchange

* It is possible to exchange multiple low cost reservations with one equal or greater costing reservation  if the price of new RI is equal or greater. It is only possible to Exchange multiple RIs for 1 new RI in one transaction
* If a reservation is transferred from one subscription to another there will be no change in reservation expiry date
* If the refund amount for the reservation is more than $50,000 USD then the  self-serve exchange option is unavailable. A support ticket needs to be created for this request and it will be reviewed by the support team and the possible options would be shared.

Learn more:

* [Cancel, exchange or refund reservations](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance#cancel-exchange-or-refund-reservations)
* [Self-service exchange and refund for Azure Reservations](https://azure.microsoft.com/blog/self-service-exchange-and-refund-for-azure-reservations/)

### Quota Increase Request
For whitelisting request, please select the below to log a case:<br>
**Issue Type**: Service and subscription limits (quotas)<br>
**Quota Type**: Compute-VM (cores-vCPUs) subscription limit increases

## **Recommended Documents**

* [Subscription Ownership transfer](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)
* [Save money on virtual machines with Azure Reserved Instances](https://docs.microsoft.com/azure/billing/billing-save-compute-costs-reservations)
* [Prepay for Virtual Machines with reserved instances](https://docs.microsoft.com/azure/virtual-machines/windows/prepay-reserved-vm-instances)
* [Understand how the reserved instance discount is applied](https://docs.microsoft.com/azure/billing/billing-understand-vm-reservation-charges)
* [Understand reserved instance usage for your Pay-As-You-Go subscription](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage)
* [Understand reserved instance usage for your Enterprise enrollment](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage-ea)
* [Windows software costs not included with reserved instances](https://docs.microsoft.com/azure/billing/billing-reserved-instance-windows-software-costs)
* [Manage reserved instances](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance)
* [Manage Microsoft Azure reservations on behalf of your customers](https://docs.microsoft.com/partner-center/azure-reservations-manage)
* [Reserved instances in Partner Center Cloud Solution Provider (CSP) program](https://docs.microsoft.com/partner-center/azure-reservations)
