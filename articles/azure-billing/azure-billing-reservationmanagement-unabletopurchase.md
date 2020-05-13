<properties
	pageTitle="reserved instance- unable to purchase or questions before purchase"
	description="reserved instance- unable to purchase or questions before purchase"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32680685"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="reserved instance- unable to purchase"
	ownershipId="ASMS_Billing"
/>

# Reserved Instance- Unable to purchase or questions before purchase

### **Unable to purchase **

You can purchase reserved instances from [Azure portal](https://portal.azure.com/#blade/Microsoft_Azure_Reservations/CreateBlade/referrer/Support_Solutions)

### **Troubleshoot purchase issues**

Please use following points to troubleshoot if you are running into issues while trying to purchase:

* You need a **Pay-As-You-Go** (3P) or **Enterprise Agreement** (17P) or Microsoft Customer Agreement subscription to purchase a reserved instance. Other subscriptions such as Azure in Open, Free Trial, MSDN, MPN, etc. **are not** eligible for RI purchase
* You _must_ have **owner** role on the subscription to buy a Reserved Instance.
* **Enterprise Agreement** billing admins can restrict the reservation purchase from EA portal. Ask your EA Admin if you’re still not able to purchase a reservation even though above conditions are met. You don’t need your partner to place the order for you.
* **Country restrictions**: Reserved Instance for Pay-As-You-Go subscriptions (03P) is **not** available in the following countries: Brazil, India, China, Taiwan, Russia, Korea, Argentina, Hong Kong, Indonesia,  Liechtenstein,  Malaysia, Mexico, Saudi Arabia, South Africa, Turkey. Please [up vote this feature request](https://feedback.azure.com/forums/170030-signup-and-billing/suggestions/37898131-make-reserved-instances-available-to-payg-subscrib). Refer [Products available by region](https://azure.microsoft.com/global-infrastructure/services/) to learn more.
* If you see a **credit card failure**, please verify if You have sufficient funds and you are using a valid payment instrument. Contact your bank if payment is declined.
* **CSP** customers can only purchase reservations through their partners. Partners can use Partner Center Portal or Azure portal for RI purchase.

### **Questions before purchase**

* **How is reservation discount applied to existing resources?**<br>
Reservation benefit automatically applies to existing resources that match the reservation SKU, region and scope. There is no tagging of a reservation to a resource. [Learn more](https://docs.microsoft.com/azure/cost-management-billing/reservations/save-compute-costs-reservations#how-reservation-discount-is-applied)

* **Which VM size should I buy?**<br>
Read this article: [Determine the right VM size before you buy](https://docs.microsoft.com/azure/virtual-machines/windows/prepay-reserved-vm-instances?toc=/azure/billing/TOC.json#determine-the-right-vm-size-before-you-buy)

* **Questions on how to buy SQL reserved capacity?**<br>
Read this article: [Buy SQL Database reserved capacity](https://docs.microsoft.com/azure/sql-database/sql-database-reserved-capacity?toc=/azure/billing/TOC.json#buy-sql-database-reserved-capacity)

* **I am in Indirect EA customer, do I need my partner to purchase?**<br>
No, you can purchase the RI if you an owner on an EA subscription.

* **Does RI purchase deduct from monetary commitment?**<br>
Yes. If you don’t have enough monetary commitment, you will get an overage invoice for the amount that exceeds the available monetary commitment.

* **How does reserved instance apply to Windows VMs or to my SQL IP costs?**<br>
The reserved instance discount only applies to the compute usage. Windows IP or SQL IP costs will be charged separately and don’t get RI discount. [Software costs not included with Azure Reserved VM Instances](https://docs.microsoft.com/azure/billing/billing-reserved-instance-windows-software-costs)

* **Questions on how to buy Reserved VM Instance?**<br>
Read these article: [Buy a Reserved VM Instance](https://docs.microsoft.com/azure/virtual-machines/windows/prepay-reserved-vm-instances?toc=/azure/billing/TOC.json#buy-a-reserved-vm-instance)<br>
Buy an instance

  1. Sign in to the [Azure portal](https://portal.azure.com/). Select **All services > Reservations**.
  2. Select **Add** to purchase a new reservation and then click **Virtual machine**.
  3. Enter required fields. Running VM instances that match the attributes you select qualify to get the reservation discount. The actual number of your VM instances that get the discount depend on the scope and quantity selected.<br>
		
Other questions: [Visit reserved instance docs](https://docs.microsoft.com/azure/billing/billing-save-compute-costs-reservations)

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
