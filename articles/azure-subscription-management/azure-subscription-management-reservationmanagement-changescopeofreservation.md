<properties
	pageTitle="Change reservation Owner or Tenant"
	description="Change reservation Owner or Tenant"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32593232,32781861"
	resourceTags=""
	productPesIds="15660,15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="2ab6a0c4-21ea-49f0-a88c-60597e4e38a3"
	ownershipId="ASMS_SubscriptionManagement"
/>

# Change Reservation Owner or Tenant
By default, the reservation purchaser and the account owner for the subscription that was used to purchase the reservation get owner access to both the reservation order and the reservations under the reservation order.

* If the user who purchased the reservation is in the organization, do the following:**

   * These users can add a user to the reservation by using the **Access Control (IAM)** tab under **Reservation**. Select the reservation, select **Reservation order** and provide access.
   * When adding users to reservations, its best to add them to the reservation order so that they can perform exchange and refunds in the future.
   * You can also add people to the reservations or reservation orders using PowerShell/CLI. See [Manage access to Azure resource using RBAC and Azure PowerShell](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-powershell).
   * To get the full list of reservations orders you have access to, see [Reservation Order -List](https://docs.microsoft.com/rest/api/reserved-vm-instances/reservationorder/list)
   * For this list, run **New-AzureRmRoleAssignment** to provide users with access to individual reservation.
   * You can also [change the reservation scope](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance#change-the-reservation-scope)<br>


* If the user who purchased the reservation is not in the organization, or if you want to change the tenant under which the reservation resides, proceed with the support ticket.<br>

The Enterprise Administrator can transfer ownership of subscriptions within an enrollment.<br>
To learn more see [Transfer Account Ownership](https://docs.azure.cn/billing/billing-subscription-transfer) in the EA portal.

### Reserved Instance Exchange

* You can exchange multiple, low-cost reservations with an equal, or greater, costing reservation if the price of a new RI is equal or greater. However, you can only exchange multiple RIs for 1 new RI in a one transaction.
* If a reservation is transferred from one subscription to another there will be no change in reservation expiry date
* If the refund amount for the reservation is more than $50,000 USD, the self-serve exchange option is unavailable. You must create a support ticket for this request, which will be reviewed by the support team.

Learn more:

* [Cancel, exchange or refund reservations](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance#cancel-exchange-or-refund-reservations)
* [Self-service exchange and refund for Azure Reservations](https://azure.microsoft.com/blog/self-service-exchange-and-refund-for-azure-reservations/)

### Quota Increase Request
For an assignment permissions request, provide the following when logging a case:<br>
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
