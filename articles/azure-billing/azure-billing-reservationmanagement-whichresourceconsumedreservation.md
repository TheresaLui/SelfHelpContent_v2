<properties
	pageTitle="reserved instance- which resource (VM, etc.) consumed the reservation"
	description="reserved instance- which resource (VM, etc.) consumed the reservation"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32680686"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="reserved instance- unable to understand usage"
	ownershipId="ASMS_Billing"
/>

# Reserved Instance- Which resource (VM, etc.) consumed the reservation

### **Reserved Instance Usage**

### **How to determine which resource (VM, etc.) consumed the reservation?**

Reserved instance discount automatically applies to your already running resource that match the reserved instance. 
You can get reservation usage information from [Azure portal](https://portal.azure.com/#blade/Microsoft_Azure_Reservations/ReservationsBrowseBlade). To see the usage data just click on the reservation that you want to check the usage for. Please note that the usage data for the current day might be incomplete, please wait for up to 24 hours to have complete utilization data.

* You can see the aggregate usage or see the usage by subscription or by resource group on this page
* You can click on the chart to see usage for a particular day in the table that’s under the chart
* You can also download the detailed usage report from the screen as well
* Please note that the reserved instance can apply to other resource sized that are in the same instance size flexibility group

Reserved instance discount is applied in the instance size flexibility ratio. [Virtual machine size flexibility with Reserved VM Instances](https://docs.microsoft.com/azure/virtual-machines/windows/reserved-vm-instance-size-flexibility)
 
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

### **Reserved Instance Usage**

You cannot request RI allocation from one region to another (e.g. East US to West US). This would need to be performed by cancelling the RI allocation and re-purchase within the desired region

* Determine RI specifications (Size, Scope, Region, Qty, Purchase Date)
* Troubleshoot RI utilization/benefit consumption
* Determine RIs aligned to account, subscription, or enrollment 

**Note**: If you cancel your subscription/resource in the middle of your billing cycle, you might still see a charge which would be for any usage in the previous month.<br>
Example, if your billing cycle was from the 26th of every month to the 25th of the next month & you suspended the subscription on the 23rd, which is 28 days into the billing cycle for June, you might see a charge for the 28 days of use. 


## **Recommended Documents**

* [Exchange and Refund policies](https://docs.microsoft.com/azure/billing/billing-azure-reservations-self-service-exchange-and-refund#exchange-policies)
* [Understand reserved instance usage for your Pay-As-You-Go subscription](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage)
* [Understand reserved instance usage for your Enterprise enrollment](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage-ea)
* [Windows software costs not included with reserved instances](https://docs.microsoft.com/azure/billing/billing-reserved-instance-windows-software-costs)
* [Manage reserved instances](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance)
* [Manage Microsoft Azure reservations on behalf of your customers](https://docs.microsoft.com/partner-center/azure-reservations-manage)
* [Reserved instances in Partner Center Cloud Solution Provider (CSP) program](https://docs.microsoft.com/partner-center/azure-reservations)
