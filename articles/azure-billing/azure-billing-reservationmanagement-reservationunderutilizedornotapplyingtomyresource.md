<properties
	pageTitle="reserved instance -reservation underutilized or not applying to my resource"
	description="reserved instance -reservation underutilized or not applying to my resource"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32690275"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="reserved instance -reservation underutilized or not applying to my resource"
	ownershipId="ASMS_Billing"
/>

# Reserved Instance -reservation underutilized or not applying to my resource

### **What to do if my reservation is underutilized?**

After purchasing a reservation, wait for up to two days to get stable usage trend for the reservation. If you continue to see lower than expected utilization try following:

* Make sure that the SKU selected for the reservation matches the deployed resource. For VMs, a reservation purchased for premium disk VM sizes will not apply to non-premium disk VMs, and vice-versa. Example: D series RI will not apply to DS series VM. Click on exchange button above to change the VM size.
* For reservations scoped to a single subscription or resource group, changing the scope can increase usage. You can [change the reservation scope](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance#change-the-reservation-scope) to shared scope or a different subscription or resource group to increase the utilization. You can also [split most reservation types](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance#split-a-single-reservation-into-two-reservations) and apply them to different scopes.
* For Virtual machine, if instance size flexibility is off, [switching it to 'on'](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance#change-optimize-setting-for-reserved-vm-instances) can potentially increase usage. Change reservation configuration.
* You can exchange the reservation to suit your changing needs. You can do a partial exchange, i.e. exchange only some of the VMs that you had purchased in the order.
 
### **How to get reservation utilization data using APIs?**

You can get reservation utilization using following APIs. Unused reservation data is also available in Azure cost analysis.

* [Reservation summaries API](https://docs.microsoft.com/rest/api/consumption/reservationssummaries/list)
* [Reservation details API](https://docs.microsoft.com/rest/api/consumption/reservationsdetails/list)
* [Get Azure consumption and reservation usage data using API](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage-ea#get-azure-consumption-and-reservation-usage-data-using-api)

Other questions: [Visit reserved instance docs](https://docs.microsoft.com/azure/billing/billing-save-compute-costs-reservations)


## **Recommended Documents**

* [Prepay for Virtual Machines with Azure Reserved VM Instances](https://docs.microsoft.com/azure/virtual-machines/windows/prepay-reserved-vm-instances#cancellations-and-exchanges )
* [Prepay for SUSE software plans from Azure Reservations](https://docs.microsoft.com/azure/virtual-machines/linux/prepay-suse-software-charges#cancellation-and-exchanges-not-allowed)
* [How return and exchange transactions are processed](https://docs.microsoft.com/azure/billing/billing-azure-reservations-self-service-exchange-and-refund#how-return-and-exchange-transactions-are-processed)
* [Exchange and Refund policies](https://docs.microsoft.com/azure/billing/billing-azure-reservations-self-service-exchange-and-refund#exchange-policies)
* [Prepay for SQL Database compute resources with Azure SQL Database reserved capacity](https://docs.microsoft.com/azure/virtual-machines/linux/prepay-suse-software-charges#cancellation-and-exchanges-not-allowed)
* [Save money on virtual machines with Azure Reserved Instances](https://docs.microsoft.com/azure/billing/billing-save-compute-costs-reservations)
* [Understand how the reserved instance discount is applied](https://docs.microsoft.com/azure/billing/billing-understand-vm-reservation-charges)
* [Understand reserved instance usage for your Pay-As-You-Go subscription](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage)
* [Understand reserved instance usage for your Enterprise enrollment](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage-ea)
* [Windows software costs not included with reserved instances](https://docs.microsoft.com/azure/billing/billing-reserved-instance-windows-software-costs)
* [Manage reserved instances](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance)
* [Manage Microsoft Azure reservations on behalf of your customers](https://docs.microsoft.com/partner-center/azure-reservations-manage)
* [Reserved instances in Partner Center Cloud Solution Provider (CSP) program](https://docs.microsoft.com/partner-center/azure-reservations)
