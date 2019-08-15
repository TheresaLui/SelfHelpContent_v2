<properties
	pageTitle="reserved instance- unable to purchase"
	description="reserved instance- unable to purchase"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32680685"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="public, Mooncake"
	articleId="reserved instance- unable to purchase"
/>

# reserved instance- unable to purchase

### **Purchase a Reserved Instance**
Please access [Reservations](https://portal.azure.com/#create/Microsoft.Reservations) in order to purchase a Reservation. Purchases of RI are only supported under **Pay-As-You-Go** (3P) and **Enterprise Agreement** (17P) offer types.<br>
**Note**: You must be in the role **Owner** on the subscription to buy a Reserved Instance. For purchasing reservations in an enterprise enrollment, the enterprise administrator must enable reservation purchases in the EA portal, by default the setting is enabled for all enrollments.<br>
Before purchasing, please check if the RI is supported for the region you are purchasing since if capacity is unavailable for a region, you will not be able to purchase RI in that region.
Reserved Instance for Pay-As-You-Go is **not** available in the following countries: Brazil, India, China, Taiwan, Russia, Korea, Argentina, Hong Kong, Indonesia,  Liechtenstein,  Malaysia, Mexico, Saudi Arabia, South Africa, Turkey.<br>
Refer [Products available by region](https://azure.microsoft.com/global-infrastructure/services/) to learn more

Additionally if you see a credit card failure, please verify if:

* You have sufficient funds
* You are using a valid Payment instrument<br>


* Virtual machines purchase experience available [here](https://docs.microsoft.com/azure/virtual-machines/windows/prepay-reserved-vm-instances).
* Determine the VM size for a customer’s Azure reservation [here](https://docs.microsoft.com/partner-center/azure-usage).
* SQL purchase experience available [here](https://docs.microsoft.com/azure/sql-database/sql-database-reserved-capacity).

### **CSP Purchase Experience**
CSP customers can only purchase reservations through their partners. RI can be purchased by Partners from both the Partner Center Portal and Ibiza.

### **Create a Reservation**

* Click **Create a resource** or **More Services**
* Search for Reservations or navigate to **Reserved VM Instances** under the **Compute** category. Click **Create**
* Fill in the **Create reservation** template to reserve VMs.
  * After all information has been entered, the cost will be automatically calculated. Cost summary will have pre-tax with comparison to original and discounted price.
* Click **Purchase** to complete the reservation

### **Fields needed to create a Reservation:**

* Name - Friendly name for the Reservation Instance.
* Subscription - This field is used to capture the subscription's PI to purchase Reservations.
* Scope - The target where the VMs will get the benefit of RI.
* Single - Only VMs running in the selected subscription will receive the RI benefit.
* Shared - All the VMs (up to the purchased RI amount) will receive the benefit under the account.
* Location/Region - Region where benefit VMs are deployed.
* VM Size - Size of VMs to receive benefit.
* VM Instance Flexibility - This will apply the Reservation discount to other VM sizes in the same VM group.
* Capacity Priority - This reserves the data center capacity for your deployments.
* Term - Reservation Duration (1 or 3 year).
* Quantity - Number of VMs that will receive benefit.

### **Discounted subscription and offer types**
Reservation discounts apply to the following eligible subscriptions and offer types. Resources that run in a subscription with other offer types don't receive the reservation discount.

1. Enterprise agreement (offer numbers: MS-AZR-0017P or MS-AZR-0148P)
2. Individual plans with pay-as-you-go rates (offer numbers: MS-AZR-0003P or MS-AZR-0023P)
3. CSP subscriptions

Learn more on how discount is applied:

  * [Reserved VM Instance](https://docs.microsoft.com/azure/billing/billing-understand-vm-reservation-charges)
  * [Cosmos DB](https://docs.microsoft.com/azure/billing/billing-understand-cosmosdb-reservation-charges)
  * [SQL Database](https://docs.microsoft.com/azure/billing/billing-understand-reservation-charges)
  * [SUSE Linux](https://docs.microsoft.com/azure/billing/billing-understand-suse-reservation-charges)

**Buy a service plan:**

* [Prepay for Cosmos DB reserved capacity](https://docs.microsoft.com/azure/cosmos-db/cosmos-db-reserved-capacity)
* [Prepay for SQL Database compute resources with Azure SQL Database reserved capacity](https://docs.microsoft.com/azure/sql-database/sql-database-reserved-capacity)
* [Prepay for Virtual Machines with Azure Reserved VM Instances](https://docs.microsoft.com/azure/virtual-machines/windows/prepay-reserved-vm-instances)

**Buy a software plan:**

* [Prepay for Red Hat software plans from Azure Reservations](https://docs.microsoft.com/azure/virtual-machines/linux/prepay-rhel-software-charges)
* [Prepay for SUSE software plans from Azure Reservations](https://docs.microsoft.com/azure/virtual-machines/linux/prepay-suse-software-charges)

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
