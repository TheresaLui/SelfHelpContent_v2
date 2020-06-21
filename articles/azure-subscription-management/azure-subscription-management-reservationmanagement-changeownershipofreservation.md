<properties
	pageTitle="Add more people to view or manage my existing reservations"
	description="Add more people to view or manage my existing reservations"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32593231"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="3e3f570d-e378-486d-ab06-cb22839030d8"
	ownershipId="ASMS_SubscriptionManagement"
/>

# Add more people to view or manage my existing reservations

## **Recommended Steps**

### **If the user who purchased the reservation is in the organization, then you can do following**

By default, the reservation purchaser and the account owner for the subscription used to purchase the reservation get owner access to the reservation order and the reservations under the reservation order.

* These users can add\other user to the reservation using the Access Control (IAM) tab under reservation. Just click on the reservation, then click on reservation order and provide access
* When adding users to reservations, its better to add them to reservation order so that they can perform exchange and refunds in future.
* You can add other people to the reservations or reservation orders using power shell / CLI. 

You can get list of all reservations orders that you have access to: [Reservation Order-List](https://docs.microsoft.com/rest/api/reserved-vm-instances/reservationorder/list)<br>

For this list execute **New-AzureRmRoleAssignment** to provide users with access to individual reservation. <br>

Read this document to learn more: [Manage access to Azure resource using RBAC and Azure PowerShell](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-powershell)<br>

_If the user who purchased the reservation is not in the organization or if you want to change the tenant under which the reservation resides then please proceed with the support ticket._<br>

Other questions: [Visit reserved instance docs](https://docs.microsoft.com/azure/billing/billing-save-compute-costs-reservations)

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

The Enterprise Administrator can transfer ownership of subscriptions within an enrollment.<br>
To learn more see [Transfer Account Ownership](https://docs.azure.cn/billing/billing-subscription-transfer) in the EA portal.<br>

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
