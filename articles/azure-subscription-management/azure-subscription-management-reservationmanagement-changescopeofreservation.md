<properties
	pageTitle="Change reservation Owner or Tenant"
	description="Change reservation Owner or Tenant"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32593232"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="2ab6a0c4-21ea-49f0-a88c-60597e4e38a3"
	ownershipId="ASMS_SubscriptionManagement"
/>

# Change Reservation Owner or Tenant

### **If the user who purchased the reservation is in the organization, then you can do following:**

By default, the reservation purchaser and the account owner for the subscription used to purchase the reservation, get owner access to the reservation order and the reservations under the reservation order.

* These users can add\other user to the reservation using the Access Control (IAM) tab under reservation. Just click on the reservation, then click on reservation order and provide access.
* When adding users to reservations, its better to add them to reservation order so that they can perform exchange and refunds in future.
* You can add other people to the reservations or reservation orders using power shell / CLI. 

You can get list of all reservations orders that you have access to: [Reservation Order -List](https://docs.microsoft.com/rest/api/reserved-vm-instances/reservationorder/list)

For this list execute **New-AzureRmRoleAssignment** to provide users with access to individual reservation. 

Read this document to learn more: [Manage access to Azure resource using RBAC and Azure PowerShell](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-powershell)

_If the user who purchased the reservation is not in the organization or if you want to change the tenant under which the reservation resides then please proceed with the support ticket._<br>

Other questions: [Visit reserved instance docs](https://docs.microsoft.com/azure/billing/billing-save-compute-costs-reservations)

Learn more: [Change reservation scope](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance#change-the-reservation-scope)<br>

The Enterprise Administrator can transfer ownership of subscriptions within an enrollment.<br>
To learn more see [Transfer Account Ownership](https://docs.azure.cn/billing/billing-subscription-transfer) in the EA portal. 

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
