<properties
	pageTitle="change ownership of reservation"
	description="change ownership of reservation"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32593231"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="public"
	articleId="3e3f570d-e378-486d-ab06-cb22839030d8"
/>

# Change ownership of reservation

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

Learn more: [Manage Reservations](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance) <br>

The Enterprise Administrator can transfer ownership of subscriptions within an enrollment. To learn more see [Transfer Account Ownership](https://ea.azure.com/helpdocs/changeAccountOwnerForASubscription) in the EA portal.<br>

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
