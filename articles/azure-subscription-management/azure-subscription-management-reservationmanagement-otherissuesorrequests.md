<properties
	pageTitle="General issues or requests for Azure Reservation Management"
	description="General issues or requests for Azure Reservation Management"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32593233"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="public"
	articleId="08b1aa47-f908-41af-b3eb-37c6e45d3dcd"
/>


# General issues or requests for Azure Reservation Management

## **Recommended Steps**

Once Azure Reservation has been purchased, you might need to apply the reservation to a different subscription, change who can manage the reservation, or change the scope of the reservation. You could also split a reservation into two reservations to apply some of the instances you bought to another subscription.

### Add or change users who can manage a reservation

You can delegate management of a reservation by adding people to roles on the reservation. By default, the person that bought the reservation and the account administrator have the Owner role on the reservation.<br>

1. Sign in to the [Azure portal](https://portal.azure.com/)
2. Select **All Services > Reservation** to list reservations that you have access to
3. Select the reservation that you want to delegate access to other users
4. Select **Access control (IAM)**
5. Select **Add role assignment > Role > Owner**. Or, if you want to give limited access, select a different role.<br>
6. Type the email address of the user you want to add as owner
7. Select the user, and then select **Save**

Learn more: [Manage Reservations](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance)<br>

The Enterprise Administrator can transfer ownership of subscriptions within an enrollment. To learn more see [Transfer Account Ownership](https://ea.azure.com/helpdocs/changeAccountOwnerForASubscription) in the EA portal. <br>

### Change Scope of a reservation

1. Sign in to the [Azure portal](https://portal.azure.com/)
2. Select **All services > Reservations**
3. Select the reservation
4. Select **Settings > Configuration**
5. Change the scope

If the scope is changed from shared to single scope, only select subscriptions where you are the owner can be selected. Only subscriptions within the same billing context as the reservation, can be selected. The scope only applies to Pay-As-You-Go offer MS-AZR-0003P or MS-AZR-0023P, Enterprise offer MS-AZR-0017P or MS-AZR-0148P, or CSP subscription types. <br>

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
