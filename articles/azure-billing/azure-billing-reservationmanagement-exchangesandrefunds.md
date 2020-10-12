<properties
	pageTitle="Cancel or change an existing reservation"
	description="Cancel or change an existing reservation"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32593227"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="0f67df6b-5123-49f6-9ab8-ff5755ec54f4"
	ownershipId="ASMS_Billing"
/>

# Cancel or change an existing reservation

* **Self-service:** You can cancel or exchange a reserved instance yourself using [Azure portal](https://portal.azure.com/#blade/Microsoft_Azure_Reservations/ReservationsBrowseBlade). Select the reservation and click on refund or exchange. Note that you must have owner access on the Reservation Order to exchange or refund. Access to only the Reservation will not let you proceed with refund or exchange. Ask the Reservation Order owner to give you owner access to the Reservation Order<br>
* **Exchange policy:** You can exchange a reservation for another reservation of the same type – there are **no penalties** on reservation exchange. The total commitment with new reservation should be greater than the sum of exchanged reservation’s refund amount and the future monthly payments (if applicable)<br>
* **Refund policy:** Sum of refund and the cancelled future payments cannot exceed $50,000 USD in a 12-month rolling window. We are **currently not charging any penalty** on refunds but could charge it on future refunds<br>
** **Exceptions:** Self-service exchange and cancel capability isn't available for US Government Enterprise Agreement customers<br>
* **API / PS / CLI** support is not available for cancellation and refunds [Self-service exchanges and refunds for Azure Reservations](https://docs.microsoft.com/azure/cost-management-billing/reservations/exchange-and-refund-azure-reservations)<br>
* Self-service exchange and cancel capability isn't available for US Government Enterprise Agreement customers. Other US Government subscription types including Pay-As-You-Go and CSP are supported

 Learn more : [How return and exchange transactions are processed](https://docs.microsoft.com/azure/billing/billing-azure-reservations-self-service-exchange-and-refund#how-return-and-exchange-transactions-are-processed)<br> 
 Learn more : [Exchange and Refund policies](https://docs.microsoft.com/azure/billing/billing-azure-reservations-self-service-exchange-and-refund#exchange-policies)<br>
Other questions: [Visit reserved instance docs](https://docs.microsoft.com/azure/billing/billing-save-compute-costs-reservations)<br>

### **Exchange an existing reserved instance (Self-service)**

You can exchange a reservation for another reservation of the same type. You can also refund a reservation, up to $50,000 USD per year, if you no longer need it. Self-service exchange and cancel capability isn't available for US Government Enterprise Agreement customers. Other US Government subscription types including Pay-As-You-Go and CSP are supported. You must have owner access on the Reservation Order to exchange or refund an existing reservation.<br>

The following steps will guide on the procedure to complete the transaction

1. Log in to your [Azure portal](https://portal.azure.com/#blade/Microsoft_Azure_Reservations/ReservationsBrowseBlade). Select the reservations that you want to refund and click **Exchange**<br>
2. Select the VM product that you want to purchase and type a quantity. Make sure that the new purchase total is more than the return total [Determine the right size before you purchase](https://docs.microsoft.com/azure/virtual-machines/windows/prepay-reserved-vm-instances#determine-the-right-vm-size-before-you-buy).<br>
3. Review and complete the transaction

### **Refund for a reserved instance**

To refund a reservation, go to **Reservation Details** and click **Refund**

### **Pro-rated refund:**

**Pro-ration and minimum requirement examples for refund and exchange**<br>
Upfront reservation example:
* You purchase a one-year term RI for $120 on January 1
* On April 7th you want to refund or exchange this reservation
* Since the reservation has been live for 97 days, you will get (1-97/365) * $120 back. (i.e. $88.1). There is currently no penalty on refunds
* If exchanging, your new purchase should be greater than $88.1
* There is no penalty on refunds currently

**Billing plan reservation example:**

* You purchase a one-year term RI for $10 per month
* On April 7th you want to refund or exchange this reservation
* Since the last payment happened 7 days, you will get (1-7/31) * $10 back. (i.e. $7.74)
* The future payments cancelled are $ 80. There is currently no penalty on refunds
* This cancellation will deduct $87.74 from you’re the $50,000 refund limit
* If exchanging, the total value of new purchase should be greater than $87.74 

## **Recommended Documents**

* [Prepay for Virtual Machines with Azure Reserved VM Instances](https://docs.microsoft.com/azure/virtual-machines/windows/prepay-reserved-vm-instances#cancellations-and-exchanges)<br>
* [Prepay for SUSE software plans from Azure Reservations](https://docs.microsoft.com/azure/virtual-machines/linux/prepay-suse-software-charges#cancellation-and-exchanges-not-allowed)<br>
* [Prepay for SQL Database compute resources with Azure SQL Database reserved capacity](https://docs.microsoft.com/azure/virtual-machines/linux/prepay-suse-software-charges#cancellation-and-exchanges-not-allowed)<br>
* [Save money on virtual machines with Azure Reserved Instances](https://docs.microsoft.com/azure/billing/billing-save-compute-costs-reservations)<br>
* [Understand how the reserved instance discount is applied](https://docs.microsoft.com/azure/billing/billing-understand-vm-reservation-charges)<br>
* [Understand reserved instance usage for your Pay-As-You-Go subscription](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage)<br>
* [Understand reserved instance usage for your Enterprise enrollment](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage-ea)<br>
* [Windows software costs not included with reserved instances](https://docs.microsoft.com/azure/billing/billing-reserved-instance-windows-software-costs)<br>
* [Manage reserved instances](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance)<br>
* [Manage Microsoft Azure reservations on behalf of your customers](https://docs.microsoft.com/partner-center/azure-reservations-manage)<br>
* [Reserved instances in Partner Center Cloud Solution Provider (CSP) program](https://docs.microsoft.com/partner-center/azure-reservations)<br>
* [How return and exchange transactions are processed](https://docs.microsoft.com/azure/billing/billing-azure-reservations-self-service-exchange-and-refund#how-return-and-exchange-transactions-are-processed)<br>
* [Exchange and Refund policies](https://docs.microsoft.com/azure/billing/billing-azure-reservations-self-service-exchange-and-refund#exchange-policies)<br>
