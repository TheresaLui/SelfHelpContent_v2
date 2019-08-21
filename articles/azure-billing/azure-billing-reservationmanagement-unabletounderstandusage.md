<properties
	pageTitle="reserved instance- unable to understand usage"
	description="reserved instance- unable to understand usage"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32680686"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="public, Mooncake"
	articleId="reserved instance- unable to understand usage"
/>

# reserved instance- unable to understand usage

### **Reserved Instance Usage**

You cannot request RI allocation from one region to another (e.g. East US to West US). This would need to be performed by cancelling the RI allocation and re-purchase within the desired region

  * Determine RI specifications (Size, Scope, Region, Qty, Purchase Date)
  * Troubleshoot RI utilization/benefit consumption
  * Determine RIs aligned to account, subscription, or enrollment 

**Note**: If you cancel your subscription/resource in the middle of your billing cycle, you might still see a charge which would be for any usage in the previous month.<br>
Example, if your billing cycle was from the 26th of every month to the 25th of the next month & you suspended the subscription on the 23rd, which is 28 days into the billing cycle for June, you might see a charge for the 28 days of use. 

### **APIs available**

  * RI Charges: [here](https://docs.microsoft.com/rest/api/billing/enterprise/billing-enterprise-api-reserved-instance-charges)
  * RI Utilization: [here](https://docs.microsoft.com/rest/api/billing/enterprise/billing-enterprise-api-reserved-instance-usage)

### **Understand usage**

  * [Understand reservation usage for your Pay-As-You-Go subscription](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage)
  * [Understand reservation usage for your Enterprise enrollment](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage-ea)
  * [Understand reservation usage for CSP subscriptions](https://docs.microsoft.com/partner-center/azure-reservations)
  * [Enterprise Agreement (EA) reservation costs and usage](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage-ea)

You can delegate reservation management by adding people to roles on the reservation order or the reservation. By default, the person that places the reservation order and the account administrator have the Owner role on the reservation order and the reservation.<br>
Learn more: [Add or change users who can manage a reservation](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance#add-or-change-users-who-can-manage-a-reservation)

## **Recommended Documents**

* [Exchange and Refund policies](https://docs.microsoft.com/azure/billing/billing-azure-reservations-self-service-exchange-and-refund#exchange-policies)
* [Understand reserved instance usage for your Pay-As-You-Go subscription](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage)
* [Understand reserved instance usage for your Enterprise enrollment](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage-ea)
* [Windows software costs not included with reserved instances](https://docs.microsoft.com/azure/billing/billing-reserved-instance-windows-software-costs)
* [Manage reserved instances](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance)
* [Manage Microsoft Azure reservations on behalf of your customers](https://docs.microsoft.com/partner-center/azure-reservations-manage)
* [Reserved instances in Partner Center Cloud Solution Provider (CSP) program](https://docs.microsoft.com/partner-center/azure-reservations)
